# fs-microbench

This is a fork of a simple filesystem microbenchmark used by Thiago Emmanuel in his file system analysis. See the original code [here](https://github.com/thiagomanel/fs-microbench).

## Run

Before running the benchmark, you need to compile the code. Go to src directory and use the following command to compile all code:

    make    

To run the benchmark:

    ./type  [THREADS] [DELAY] [NUMBER_OF_OPERATIONS] [PATH] [BLOCK_SIZE] [DEBUG] >> output.csv

where the type can be `sr`, `sw`, `rr` or `rw` and the flags:

    - THREADS: set the number of threads
    - DELAY: represents the interval between requests
    - NUMBER_OF_OPERATIONS: set the number of operations
    - PATH: is the path of the file that we will do the operations. This file needs to exist before running the command. You should create the file ~/file0 with the required size. 
    - BLOCK_SIZE: set the block size
    - DEBUG: that must be 'debug' or 'no-debug'

## Output

The output is a csv file that contains:

    id_thread, id_req, begin_timestamp, end_timestamp, offset, count_bytes

## Example

    ./sr 1 0 5000 ~/file 4096 debug >> output.csv

Example of a sequential read benchmark with 1 thread, no interval between requests, 5000 requests on ~/file0, a block size of 4096 and the debug mode on. This is not a typing error, you should create a ~/file0 before running and reference it as ~/file.
