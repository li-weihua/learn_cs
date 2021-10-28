docker
=======

dockerfile cannot link libcuda.so problem
--------------------------------------------

The default runtime used by docker is ``runc``, so one can set /etc/docker/daemon.json
::
    
    "default-runtime": "nvidia",

It is also the only way to have GPU access during docker build.