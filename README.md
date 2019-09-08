# grpc_example
A toy example following the grpc.io docs


Steps:
1. pip install grpcio
2. pip install grpcio-tools

# Example work
Go here https://grpc.io/docs/quickstart/python/ and clone this repo to play with examples `clone -b v1.23.0 https://github.com/grpc/grpc`

## Example 1: HelloWorld
Run a server, run a client (stub), add a new method to server for client to call.
* tree of `my_helloworld` directory
```bash
..
├── protos
│   └── helloworld.proto
└── python
    ├── __pycache__
    │   ├── helloworld_pb2.cpython-37.pyc
    │   └── helloworld_pb2_grpc.cpython-37.pyc
    ├── greeter_client.py
    ├── greeter_server.py
    ├── helloworld_pb2.py
    └── helloworld_pb2_grpc.py
```

* this involves updating the .proto layer
* then compiling the grpc code with `python -m grpc_tools.protoc -I ../protos --python_out=. --grpc_python_out=. ../protos/helloworld.proto`


_Notes_
* The imported modules `helloworld_pb2` and `helloworld_pb2_grpc` are auto-generated code.
* `helloworld_pb2.py` seems to be formal python configurations definitions of the .proto
    * `*_pb2.py` contains generated _request_ and _response_ classes
* `helloworld_pb2_grpc.py` seems to be Python code (classes/funcs)
    * `*_pb2_grpc.py` contains generated _client_ and _server_ classes
