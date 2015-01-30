JIC is written in Python 2.7 and uses jira-python library.

To install all the dependencies do the following as root:

1. install setuptools

    e.g. for debian testing that can be done as:

        $ sudo apt-get install python2.7-setuptools libpython2.7-dev python2.7-dev

    If your Linux does not have such a package available, see
    http://www.pip-installer.org/en/latest/installing.html


1. install pip

    e.g. for debian testing that can be done as:

        $ sudo apt-get install python-pip

    If your Linux does not have such a package available, see
    http://www.pip-installer.org/en/latest/installing.html


1. install oauth2 (needed for OAuth)

    $ sudo apt-get install python-oauth2

    OR

    $ sudo pip install oauth2


1. install requests-oauthlib (needed for OAuth)

    $ sudo pip install requsts-oauthlib


1. install jira.python

    $ sudo pip install jira-python


1. install pycrypto (needed for OAuth)

    $ sudo pip install pycrypto


    NOTE: if you get the following error message during the
    installation, make sure your TMP env var is pointing to the location
    which can be used to execute binaries from:

    """
        checking whether we are cross compiling... configure: error: in
            `/tmp/pip-build-root/pycrypto':

        configure: error: cannot run C compiled programs.

    """

    To do that use something like:

        # mkdir ./tmp
        # TMP=./tmp pip install pycrypto
        # rm -Irf ./tmp


1. optional - install keyring module

    If you would like to use your keyring manager to store your JIRA
    password intead of using OAuth or storing it in config in plain text
    format, you may want to install `keyring` module. If that module is
    available on the system and OAuth in not configured, jic will use
    keyring store to store passwords.

    $ sudo pip install keyring


1. optional - install python-magic

    If you're getting the following error

        Traceback (most recent call last):
          File "./jic", line 1532, in <module>
            main()
          File "./jic", line 1529, in main
            exit(cmd(cfg, args[2:]))
          File "./jic", line 578, in cmd_list_issues
            jira = get_jira(cfg)
          File "./jic", line 1493, in get_jira
            jira = JIRA(options=options, basic_auth=auth)
          File "/usr/local/lib/python2.7/dist-packages/jira/client.py", line
        104, in __init__
            self._try_magic()
          File "/usr/local/lib/python2.7/dist-packages/jira/client.py", line
        1437, in _try_magic
            self._magic = magic.Magic(mime=True)
        TypeError: __init__() got an unexpected keyword argument 'mime'

    try installing python-magic (using pip, not apt-get):

    $ sudo pip install python-magic


1. Put `config` file into ~/.jic/


1. Create symlinks for the porcelain mode commands

    $ jic commands symlink


On the first attempt to run jic it will try to import the existing
config at ~/.jicrc. Please use the example config provided to create
your own config.
