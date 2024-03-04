# FlashInfer

Flashinfer with built in page fault recovery via ECC

## Run Benchmarks

We profile FlashInfer kernel performance with [nvbench](https://github.com/NVIDIA/nvbench) and you can compile and run the benchmarks with the following commands:

```bash
mkdir build
cp cmake/config.cmake build # you can modify the config.cmake to enable/disable benchmarks and change CUDA architectures
cd build
cmake ..
make -j12
```

You can run `./bench_{single/batch}_{prefill/decode}` to benchmark the performance (e.g. `./bench_single_prefill` for single-request prefill attention). `./bench_{single/batch}_{prefill/decode} --help` will show you the available options. 

## C++ API and TVM Bindings

FlashInfer also provides C++ API and TVM bindings, please refer to [documentation](https://docs.flashinfer.ai/) for more details.

## Adoption

Currently FlashInfer is adopted by the following projects:
- [MLC-LLM](https://github.com/mlc-ai/mlc-llm)
- [Punica](https://github.com/punica-ai/punica)
- [sglang](https://github.com/sgl-project/sglang)

## Acknowledgement

FlashInfer is inspired by [FlashAttention 1&2](https://github.com/dao-AILab/flash-attention/), [vLLM](https://github.com/vllm-project/vllm), [stream-K](https://arxiv.org/abs/2301.03598) and [cutlass](https://github.com/nvidia/cutlass) projects.
