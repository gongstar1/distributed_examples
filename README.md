# distributed_examples
## single node
### **pytorch DDP**
```
CUDA_VISIBLE_DEVICES=0,1 python pytorch_ddp_mnist.py -a resnet50 --dist-url 'tcp://127.0.0.1:40002' --dist-backend 'nccl' --multiprocessing-distributed --world-size 1 --rank 0
```
### **horovod**
```
CUDA_VISIBLE_DEVICES=0,1 horovodrun  -np 2 -H localhost:2 python horovod_pytorch_mnist.py
```
