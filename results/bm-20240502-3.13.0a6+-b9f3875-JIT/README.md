# Results

- fork: brandtbucher
- version: 3.13.0a6+
- config: JIT
- commit hash: [b9f3875](https://github.com/brandtbucher/cpython/commit/b9f3875)
- commit date: 2024-05-02T16:38:06-07:00
- commit merge base: [c408c36e9b346f9f15a34e98a5596f311df65efa](https://github.com/brandtbucher/cpython/commit/c408c36e9b346f9f15a34e98a5596f311df65efa)
- ref: exits

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8933042107)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6%2B-b9f3875.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6%2B-b9f3875-vs-3.10.4.md)
- [📈time plot](bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6%2B-b9f3875-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 97.80%, 1.00x faster at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6%2B-b9f3875-vs-3.12.0.md)
- [📈time plot](bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6%2B-b9f3875-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.00x faster (HPT: reliability of 87.30%, 1.00x slower at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6%2B-b9f3875-vs-3.13.0b2.md)
- [📈time plot](bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6%2B-b9f3875-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 94.86%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6%2B-b9f3875-vs-base-mem.svg)
- [📄table](bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6%2B-b9f3875-vs-base.md)
- [📈time plot](bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6%2B-b9f3875-vs-base.svg)

