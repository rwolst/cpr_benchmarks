# C vs Python vs Rust
Test the speed in scientific computing for the above languages. Communication
is performed through RAM files and messages are sent using a RabbitMQ server in
a docker container. The tests are as follows (and should be parallelsied where
possible):

  1. Assigning to an array.
  2. Exponentiating values in an array.
  3. Sampling from uniform distribution.
  4. Matrix matrix multiplication (one).
  5. Matrix vector multiplication (many).
  6. Simulation of simple game (with softmax and sampling).
  7. Simulation of simple game with message reading from RabbitMQ.

## Installation
To do. Requires both installation of Python packages into virtual environment
AND downloading of C libraries into `./libs`.

The only currently used library is `libcsv` which can be downloaded in `./libs`
with

    git clone git@github.com:rgamble/libcsv.git
    cd libcsv
    autoreconf -f -i
    ./configure
    make

There is no need to install. I am also not sure if `autoreconf` is always
necessary, but I needed for my system.
