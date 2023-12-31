# Academic Website

This repository contains source code of my academic/personal website purely layouted in boostrap.
See demo at [https://tuandang.info](https://tuandang.info/) using Jekyll as a static website generator. Feel free to clone this code for your personal use!

The good thing about making personal website using Jekyll are:
1. No database: Store your data in **yaml** format (see example below)
2. Separate data from view: If you want to add more information, just add into file yaml and forget about html/layout when you done with html/layout.

Example:

Data stored in file **review_conf.yml**
```
- link: https://2024.ieee-icra.org
  conf: IEEE International Conference on Robotics and Automation (ICRA 2024)

- link: https://ieee-iros.org
  conf: The 2023 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS 2023)

- link: https://wacv2024.thecvf.com
  conf: Winter Conference on Applications of Computer Vision (WCACV 2024)

- link: https://feee-conf.com/isee2023
  conf: The 2023 International Symposium on Electrical and Electronics Engineering (ISEE 2023, 6 papers)

- link: https://link.springer.com/conference/aciids
  conf: Asian Conference on Intelligent Information and Database Systems (14th, 15th)

```

Display in **html code**

```
<h5 class="mb-0">Review conferences</h5> <br>
<ul>
{% for item in site.data.review_conf %}
  <li><a href="{{item.link}}">{{item.conf}}</a></li>
{% endfor %}
</ul>   
```

<!-- <p align="center">
  <img src="assets/img/website.png" width="600"/><br/>
</p> -->


## Prerequisites

* [Ruby with DevKit](https://rubyinstaller.org/downloads/) (version in use 3.2.2-1)
* [Jekyll](https://jekyllrb.com/) (version  in use 4.3.2).

After installing Ruby, Jekyll can be installed via the following command:

```
gem install bundler jekyll 
```

Now, you can use Jekyll locally as a website (static) generator on your laptop.

<!-- USAGE -->

## Usage

### Clone the repository

```
git clone https://github.com/tuantdang/academic_website.git
cd academic-website
```

### Customize personal information

When opening the code from an IDE, you should see a structure like this:

```
.
├───assets                      # folder including your images, files, etc
├───_data                       # yaml static data              
├───_layouts      
|   └───default.html            # the default layout  
├───_site                       # static output for deployment
├───index.md                    # file to generate index.html
|───portfolio.md                # file to generate portfolio.html
└───_config.yml                 # information for webpage title and favicon
```

You can modify the `_config.yml` file to your information:

### Add moore page
You can add more papges like portofiio.md to generate portofiio.html in folder _site.

###  Run the webpage at localhost

After changing to your information, the website can be tested using the following command:

```
bundle exec jekyll server
```

You can either see the web version in the `_site/index.html` file or go to your `localhost`: [http://localhost:4000](http://localhost:4000).

## Deploy the webpage at your desired host
Copy folder _site to your host and enjoy!

