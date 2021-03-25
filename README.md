# Aims and Goals

This GitHub repository is my method of learning how to use `git` version control and GitHub. By using GitHub to manage my:

* Markdown lecture notes
* Assignments
* Tutorials

I should get to hang with `git` commands and the GitHub service.

# Recommended Use
To view the GitHub pages site generated by this repository, go to: [bweston6.github.io/UoL](https://bweston6.github.io/UoL/).

# Build
To build this site manually use the following instructions for *Arch Linux*. For more general instructions, refer to [Testing your GitHub Pages site locally with Jekyll](https://docs.github.com/en/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll). To start, clone the repository.

1. Install Ruby and RubyGems:
	
	```
	# pacman -S rubygems base-devel
	```
1. Install Bundler:
	
	```
	$ gem install bundler
	```
1. Add the RubyGem intall directory to your `PATH`:

	```
	$ export PATH="$HOME/.local/share/gem/ruby/2.7.0/bin:$PATH"
	```
	
	This is only required if you were prompted by `gem` to do so in step 2. To set this permanently, add this line to the end of your `bashrc` or equivalent and then `source` the file.
1. Navigate to `/docs` and run `bundle` to install the site dependencies:

	```
	$ cd docs
	$ bundle install
	```
	
	This may take several minutes to complete.
1. To build the site run:

	```
	$ bundle exec jekyll serve
	```
	
	This may also take some time to run due to the number of posts.
	
	This will build the site in the folder `/docs/_site`. You can also preview the site at `http://localhost:4000/UoL/`. Make sure to remember the trailing slash.
	
# File Organisation
All source files are located in `/docs`. To make accessing these files easier on desktop, they are symlinked by folders in each module. This structure doesn't work well on [github.com](https://github.com/bweston6/UoL) as the links are treated as files. 
