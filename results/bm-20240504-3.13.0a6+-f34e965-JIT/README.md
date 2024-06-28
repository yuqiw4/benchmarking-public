# Results

- fork: python
- version: 3.13.0a6+
- config: JIT
- commit hash: [f34e965](https://github.com/python/cpython/commit/f34e965)
- commit date: 2024-05-04T07:44:49-07:00
- commit merge base: [f6b5d3bdc83f8daca05e8b379190587a236585ef](https://github.com/python/cpython/commit/f6b5d3bdc83f8daca05e8b379190587a236585ef)
- ref: f34e965e52b9bdf157b8

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8951900451)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240504-linux-x86_64-python-f34e965e52b9bdf157b8-3.13.0a6%2B-f34e965.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: docutils, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240504-linux-x86_64-python-f34e965e52b9bdf157b8-3.13.0a6%2B-f34e965-vs-3.10.4.md)
- [📈time plot](bm-20240504-linux-x86_64-python-f34e965e52b9bdf157b8-3.13.0a6%2B-f34e965-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 95.57%, 1.00x faster at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: docutils, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240504-linux-x86_64-python-f34e965e52b9bdf157b8-3.13.0a6%2B-f34e965-vs-3.12.0.md)
- [📈time plot](bm-20240504-linux-x86_64-python-f34e965e52b9bdf157b8-3.13.0a6%2B-f34e965-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.00x faster (HPT: reliability of 68.17%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: bpe_tokeniser, docutils
- [📄table](bm-20240504-linux-x86_64-python-f34e965e52b9bdf157b8-3.13.0a6%2B-f34e965-vs-3.13.0b2.md)
- [📈time plot](bm-20240504-linux-x86_64-python-f34e965e52b9bdf157b8-3.13.0a6%2B-f34e965-vs-3.13.0b2.svg)

