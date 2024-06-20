# Results

- fork: brandtbucher
- version: 3.13.0a6+
- config: JIT
- commit hash: [f7a4afd](https://github.com/brandtbucher/cpython/commit/f7a4afd)
- commit date: 2024-04-23T14:49:14-07:00
- commit merge base: [2e7771a03d8975ee8a9918ce754c665508c3f682](https://github.com/brandtbucher/cpython/commit/2e7771a03d8975ee8a9918ce754c665508c3f682)
- ref: justin_ghccc_perf

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8808142633)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6%2B-f7a4afd.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6%2B-f7a4afd-vs-3.10.4.md)
- [📈time plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6%2B-f7a4afd-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 98.27%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6%2B-f7a4afd-vs-3.12.0.md)
- [📈time plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6%2B-f7a4afd-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x faster (HPT: reliability of 96.77%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6%2B-f7a4afd-vs-3.13.0b2.md)
- [📈time plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6%2B-f7a4afd-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6%2B-f7a4afd-vs-base-mem.svg)
- [📄table](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6%2B-f7a4afd-vs-base.md)
- [📈time plot](bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6%2B-f7a4afd-vs-base.svg)

