To build locally:
=================

* Install [Sphinx](http://www.sphinx-doc.org/en/stable/install.html)
* sudo pip install sphinx
* sudo pip install sphinx-tabs
* Run the command ```sphinx-build -n . _build``` in this directory.
* Open the file _build/index.html in your browser to view.

For Cecily:
===========
If you've restarted your computer and get the 'command not found' message, add sphinx back to your path:
* Get location: pip show sphinx
* Add to path: export PATH="/Users/thebeast/Library/Python/2.7/lib/python/site-packages:$PATH"
* Reload the bash_profile: source ~/.bash_profile
* Make sure it's working now: sphinx-build --version

To deploy:
==========

* build the docs:
```sphinx-build -n . _build```
* check the build
* remove the cached build files
```rm -fr .doctrees```
* move the build out of the repo dir:
```rm -r /tmp/_build; mv _build /tmp```
* check out the gh-pages branch:
```git checkout gh-pages && git pull```
* remove previous files:
```rm -r *```
* move new files in:
```mv /tmp/_build/* .```
* add the github domain name file:
```echo 'docs.repairtagger.com' > ./CNAME```
* commit and push:
```git add . && git commit -m 'Updated docs' && git push```
