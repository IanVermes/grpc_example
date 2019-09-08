# grpc_example
A toy example following the grpc.io docs


Steps:
1. pip install grpcio
2. pip install grpcio-tools

# Example work
Go here https://grpc.io/docs/quickstart/python/ and clone this repo to play with examples `clone -b v1.23.0 https://github.com/grpc/grpc`

## Example 1: HelloWorld
Run a server, run a client (stub), add a new method to server for client to call.
* this involves updating the .proto layer
* then compiling the grpc code with `python -m grpc_tools.protoc -I ../protos --python_out=. --grpc_python_out=. ../protos/helloworld.proto`

_Notes_<br>
* The imported modules `helloworld_pb2` and `helloworld_pb2_grpc` are auto-generated code.
* `helloworld_pb2.py` seems to be formal python configurations definitions of the .proto
* `helloworld_pb2_grpc.py` seems to be Python code (classes/funcs)
