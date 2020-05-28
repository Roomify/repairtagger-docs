To build locally:

* Install [Sphinx](http://www.sphinx-doc.org/en/stable/install.html)
* Run the command ```sphinx-build -n . _build``` in this directory.
* Open the file _build/index.html in your browser to view.

For Cecily:
If you've restarted your computer and get the 'command not found' message, add sphinx back to your path:
* Get location: pip show sphinx
* Add to path: export PATH="/Users/thebeast/Library/Python/2.7/lib/python/site-packages:$PATH"
* Reload the bash_profile: source ~/.bash_profile
* Make sure it's working now: sphinx-build --version
