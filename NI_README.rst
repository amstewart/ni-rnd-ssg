NOTE: I don't use Windows, so everything below that is linux specific is my best
guess. If you find anything wrong, just amend it in the readme and submit a pull
request.

============
INSTALLATION
============

1. Get the python ``virtualenv`` utility suite from somewhere.

* On Debian and similar linux distros, ``apt install virtualenv``
    * Then ``virtualenv venv`` to create the virtual environment in your repo
    * ``source ./venv/bin/activate`` to drop into the virtual environment
* On Windows, I think you have to install virtualenv through pip. 
and pip and then the virtualenvwrapper for powershell. I suppose, follow the
instructions here:

http://www.tylerbutler.com/2012/05/how-to-install-python-pip-and-virtualenv-on-windows-with-powershell/

2. Once you are in your virtual environment shell, install the requirements from
``:requirements.txt``

``pip install -r requirements.txt``

Note that the install might still fail because you lack certain system binaries.
For example, my install required that I pick up a Fortran compiler which, in my
case, meant installing the ``gfortran`` debian package.

You can always continue the installation by recalling the pip install command
above.

3. Once all your python packages are up to date. Start the jupyter notebook
server using the following command:

``jupyter notebook --configure=serer-config.py``

This should start hosting the jupyter notebook on the address 'localhost'. You
can now connect to it by browsing to: http://localhost:8888

I've set the default password for the server to 'qweqwe'. As of jupyter 5, there
it isn't recommended that you configure the server to allow anonymous access,
since you're basically providing privilaged access to your filesystem.

But if you want to change the notebook password, you need to recalculate a new
hash using the process outlined in :server-config.py:210.

=========
EXERCISES
=========

Copy (ie. 'duplicate') the chapter ipynotebook file when you go to complete the
exercises. Then you can push your new file without it conflicting with the
group work or with the original ipynotebook file.
