# Results

- fork: python
- version: 3.13.0a6+
- config: JIT
- commit hash: [3e06c7f](https://github.com/python/cpython/commit/3e06c7f)
- commit date: 2024-04-26T18:08:50+01:00
- commit merge base: [63add11704078390909a485b57a7de6a0358fc2b](https://github.com/python/cpython/commit/63add11704078390909a485b57a7de6a0358fc2b)
- ref: 3e06c7f719b99cc7f5e8

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8853587364)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240426-linux-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-linux-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f-vs-3.10.4.md)
- [📈time plot](bm-20240426-linux-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 90.75%, 1.00x faster at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-linux-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f-vs-3.12.0.md)
- [📈time plot](bm-20240426-linux-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 99.67%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240426-linux-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f-vs-3.13.0b2.md)
- [📈time plot](bm-20240426-linux-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f-vs-3.13.0b2.svg)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8853587364)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f.json)

### vs. 3.10.4

- Geometric mean: 1.26x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f-vs-3.10.4.md)
- [📈time plot](bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.02x slower (HPT: reliability of 97.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f-vs-3.12.0.md)
- [📈time plot](bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.02x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f-vs-3.13.0b2.md)
- [📈time plot](bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6%2B-3e06c7f-vs-3.13.0b2.svg)

