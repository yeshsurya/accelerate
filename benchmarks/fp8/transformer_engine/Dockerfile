FROM nvcr.io/nvidia/pytorch:23.06-py3

RUN pip install transformers evaluate datasets
RUN pip install deepspeed
RUN pip uninstall transformer_engine
RUN pip install git+https://github.com/NVIDIA/TransformerEngine.git@stable
RUN pip install --upgrade torch torchvision torchtext torchdata torch-tensorrt flash-attn 
RUN pip install mpi4py
RUN pip install fbgemm_gpu
RUN git clone https://github.com/huggingface/accelerate.git

RUN cd accelerate && \
    pip install -e . && \
    cd benchmarks/fp8

RUN /bin/bash


