Usage
=====

.. _installation:

Installation
------------

To use Sap2000py, first install it using pip:

.. code-block:: console

   (.venv) $ pip install Sap2000py

Creating Sap2000 Project Object
----------------

To create a Saproject(Sap2000 Project Object), you can use the ``openSap`` function:

.. autofunction:: Sap2000py.openSap
   

you can change settings by passing parameters to ``createSap`` function:

.. autofunction:: Sap2000py.createSap


.. _usage:

if ``AttachToInstance`` = True , attatch the pointer to a running API instance, otherwise open a new instance
if ``SpecifyPath`` is set to True, then ProgramPath to your SAP2000 program should be specified
-----

Open a Sap2000 program interface
----------------

To Open a Sap2000 program, use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

