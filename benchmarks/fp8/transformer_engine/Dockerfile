FROM nvcr.io/nvidia/pytorch:23.06-py3

RUN pip install transformers evaluate datasets
RUN pip install deepspeed
RUN pip install git+https://github.com/NVIDIA/TransformerEngine.git@stable
RUN pip install --upgrade torch torchvision torchtext torchdata torch-tensorrt flash-attn 
RUN git clone https://github.com/huggingface/accelerate.git

RUN cd accelerate && \
    pip install -e . && \
    cd benchmarks/fp8

RUN /bin/bash


