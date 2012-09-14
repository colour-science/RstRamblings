Manager
=======

..  image:: https://secure.travis-ci.org/KelSolaar/Foundations.png?branch=master

Introduction
------------

Manager is the Components Manager package of `Umbra <https://github.com/KelSolaar/Umbra>`_, `sIBL_GUI <https://github.com/KelSolaar/sIBL_GUI>`_ and `sIBL_Reporter <https://github.com/KelSolaar/sIBL_Reporter>`_. Components are simple python packages extending capabilities of their host application.

Installation
------------

To install **Manager** from the `Python Package Index <http://pypi.python.org/pypi/Manager>`_ you can issue this command in a shell::

	pip install Manager

or this alternative command::

	easy_install Manager

Alternatively, if you want to directly install from `Github <http://github.com/KelSolaar/Manager>`_ source repository::

	git clone git://github.com/KelSolaar/Manager.git
	python setup.py install

Usage
-----

A Component package contains at least a resource description file and a main module::

	├── testsComponentA
	│   ├── __init__.py
	│   ├── __init__.pyc
	│   ├── testsComponentA.py
	│   ├── testsComponentA.pyc
	│   └── testsComponentA.rc

	>>> manager = Manager(("./manager/tests/testsManager/resources/components/core",))
	>>> manager.registerComponents()
	True
	>>> manager.listComponents()
	['core.testsComponentA', 'core.testsComponentB']
	>>> manager.instantiateComponents()
	True
	>>> manager.getInterface("core.testsComponentA")
	<testsComponentA.TestsComponentA object at 0x11dd990>

About
-----

| Manager by Thomas Mansencal Ð 2008 - 2012
| Copyright© 2008 - 2012 Ð Thomas Mansencal Ð `thomas.mansencal@gmail.com <mailto:thomas.mansencal@gmail.com>`_
| This software is released under terms of GNU GPL V3 license: http://www.gnu.org/licenses/
| `http://www.thomasmansencal.com/ <http://www.thomasmansencal.com/>`_
