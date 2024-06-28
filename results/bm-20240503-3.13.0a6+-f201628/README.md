# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [f201628](https://github.com/python/cpython/commit/f201628)
- commit date: 2024-05-03T00:51:43+00:00
- commit merge base: [f8290df63f1fd970dfd6bbfdc9a86341a9f97d05](https://github.com/python/cpython/commit/f8290df63f1fd970dfd6bbfdc9a86341a9f97d05)
- ref: f201628073f22a785a09

## linux x86_64 (azure)

- [pystats raw](bm-20240503-azure-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-pystats.json)
- [pystats table](bm-20240503-azure-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8941340909)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.10.4.md)
- [📈time plot](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.96%, 1.01x faster at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.12.0.md)
- [📈time plot](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x faster (HPT: reliability of 99.80%, 1.00x faster at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: bpe_tokeniser
- [📄table](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.13.0b2.md)
- [📈time plot](bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.13.0b2.svg)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8941698099)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628.json)

### vs. 3.10.4

- Geometric mean: 1.28x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.10.4.md)
- [📈time plot](bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.00x slower (HPT: reliability of 59.27%, 1.00x slower at 99th %ile)
- Memory usage: 0.92x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.12.0.md)
- [📈time plot](bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.00x slower (HPT: reliability of 98.90%, 1.00x slower at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: bpe_tokeniser
- [📄table](bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.13.0b2.md)
- [📈time plot](bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6%2B-f201628-vs-3.13.0b2.svg)

