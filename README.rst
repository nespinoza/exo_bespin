Installation
------------

The following are instructions on how to install the ``exo_bespin`` package for both users and contributors.  The ``exo_bespin`` repository provides a ``conda`` environment containing all of the dependencies needed to install and execute the ``exo_bespin`` software.


Download Anaconda or Miniconda
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You must first have a working installation of ``anaconda`` or ``miniconda`` for Python 3.  If you do not yet have this on your system, you can visit the following links for download and installation instructions:

- `Anaconda <https://www.anaconda.com/download/>`_
- `Miniconda <https://conda.io/en/latest/miniconda.html>`_


Obtain the ``exo_bespin`` Package
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To obtain the ``exo_bespin`` package with the necessary environment files, clone the repository directly from GitHub:

::

  git clone https://github.com/exo-bespin/exo_bespin.git
  cd exo_bespin


Environment Installation
~~~~~~~~~~~~~~~~~~~~~~~~
You can install the Exo-Bespin ``conda`` environment via the ``environment.yml`` file.  First, one should ensure that their version of ``conda`` is up to date:

::

  conda update conda


Next, one should activate the ``base`` environment:

::

  conda activate base


Next, one can create the ``exo-bespin`` ``conda`` environment via the ``environment.yml`` file:

::

  conda env create -n exo-bespin -f environment.yml


Lastly, one can activate the newly-created environment with:

::

  conda activate exo-bespin


Package Installation
~~~~~~~~~~~~~~~~~~~~

In order to install the ``exo_bespin`` package within the newly-created ``conda``
environment, run the ``exo_bespin`` setup script:

::

  python setup.py develop


``aws_config.json`` File
~~~~~~~~~~~~~~~~~~~~~~~~

Users that wish to utilze the ``aws`` subpackage must have an ``aws_config.json``
file within the ``exo_bespin/aws`` directory in the local installation locataion.
Below is a template of the contents of this file:

::

  {
   "ec2_id" : "",  # EC2 instance ID or EC2 Launch Template ID
   "key_pair_name": "",  # Name of the SSH key/pair used to connect to EC2
   "security_group_id": "",  # ID of security group used to connect to EC2
   "ssh_file" : ""  # Path to public SSH key
  }


Missing Dependencies?
~~~~~~~~~~~~~~~~~~~~~
If you find that the ``exo-bespin`` ``conda`` environment is missing a required dependency, please feel free to `submit a GitHub Issue <https://github.com/exo-bespin/exo_bespin/issues>`_ detailing the problem.
