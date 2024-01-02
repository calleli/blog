# blog
A place where i jot stuff down that also might be of interest to others 


## How did i configure this site?
 1. Create a new github repository
 1. Clone the repository to local machine 
 1. Make sure you have [Ruby](https://www.ruby-lang.org/en/) installed.  
    I am using [rbenv](https://github.com/rbenv/rbenv) as my ruby version manager to install and select what ruby version to use on my machine.
 1. Install a high enough Ruby version. When trying the steps below, i got warned that i needed a Ruby version higher than `3.0.0`.  
    To fix that, do the following:  
    Make sure you sucessfully installed `Rbenv` by running:
    ```bash
    rbenv -v
    ```
    You should see something like: 
    ```bash
    rbenv 1.2.0-11-ge4f61e6
    ```
    Now install a ruby version, for example: 
    ```bash
    rbenv install 3.1.1
    ```
    You should now see the new version installed. Confirm by running:  
    ```bash
    rbenv versions
    ```
    You should now see something like:  
    ```bash
    system
    * 2.7.5 (set by /home/YOUR_USERNAME/.ruby-version)
    3.1.1
    ```
    Change to the new Ruby version by:  
    ```bash
    rbenv global 3.1.1   # set the default Ruby version for this machine
    # or:
    rbenv local 3.1.1    # set the Ruby version for this directory
    ```
    Update [Rubygems](https://rubygems.org/)
     ```bash
    gem update --system
    ```
 1. Initialize a [Bundler](https://bundler.io/) 
    ```bash 
    bundle init
    ```
 1. Set up install path for the gems used in the project 
    ```bash
    bundle config set --local path 'vendor/bundle'
    ```
 1. Add [Jekyll](https://jekyllrb.com/) to the bundler 
    ```bash
    bundle add jekyll
    ```
  1. Scaffold the site 
     ```bash
     bundle exec jekyll new --force --skip-bundle .
     bundle install
     ```
  1. Run your site locally:
     ```bash
     bundle exec jekyll serve
     ```
  
