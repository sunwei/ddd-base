DDD base framework for python
=============================

|Build Status| |Pypi Status| |Coveralls Status|

Installation
------------

From source code:

::

   python setup.py install

From pypi:

::

   pip install ddd-base

Usage
-----

::

   from ddd_base.value_object import ValueObject


   class TestValueObject(ValueObject):

       def __init__(self, name):
           super().__init__()
           self.name = name

       def __eq__(self, other):
           if not isinstance(other, ValueObject):
               return NotImplemented

           return self.name == other.name


   def mytest():
       print("Testing...")
       a_value_object = TestValueObject("name")
       b_value_object = TestValueObject("name")

       print(a_value_object.same_as(b_value_object))

   if __name__ == '__main__':
       mytest()


License
-------

This software is licensed under the `MIT license <http://en.wikipedia.org/wiki/MIT_License>`_

See `License file <https://github.com/sunwei/ddd-base/blob/master/LICENSE>`_

.. |Build Status| https://travis-ci.com/sunwei/ddd-base.svg?branch=master
   :target: https://travis-ci.com/sunwei/ddd-base
.. |Pypi Status| image:: https://badge.fury.io/py/envoy-webhook-auth-decorator.svg
   :target: https://badge.fury.io/py/envoy-webhook-auth-decorator
.. |Coveralls Status| image:: https://coveralls.io/repos/github/sunwei/ddd-base/badge.svg?branch=master
   :target: https://coveralls.io/github/sunwei/ddd-base?branch=master
