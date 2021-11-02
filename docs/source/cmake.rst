cmake
======

How to add ``protobuf`` as a third_party library?
---------------------------------------------------

There are two methods:

#. use cmake `ExternalProject_Add`_, see `cmake_protobuf_example1`_.

#. use protobuf as third_party library directly, and write cmake macro or function to 
   handle link libraries and compile proto files, see `cmake_protobuf_example2`_.


.. _ExternalProject_Add: https://cmake.org/cmake/help/latest/module/ExternalProject.html
.. _cmake_protobuf_example1: https://github.com/li-weihua/cmake_protobuf_example1
.. _cmake_protobuf_example2: https://github.com/li-weihua/cmake_protobuf_example2
