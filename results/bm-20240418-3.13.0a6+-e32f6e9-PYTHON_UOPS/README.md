# Results

- fork: python
- version: 3.13.0a6+
- config: T2
- commit hash: [e32f6e9](https://github.com/python/cpython/commit/e32f6e9)
- commit date: 2024-04-18T11:09:30+01:00
- commit merge base: [f70395786f6da2412d7406606feb64347fc71262](https://github.com/python/cpython/commit/f70395786f6da2412d7406606feb64347fc71262)
- ref: e32f6e9e4b202ce8759b

## linux x86_64 (azure)

- [pystats raw](bm-20240418-azure-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6%2B-e32f6e9-pystats.json)
- [pystats table](bm-20240418-azure-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6%2B-e32f6e9-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8736177709)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6%2B-e32f6e9.json)

### vs. 3.10.4

- Geometric mean: 1.07x faster (HPT: reliability of 86.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6%2B-e32f6e9-vs-3.10.4.md)
- [📈time plot](bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6%2B-e32f6e9-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.21x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6%2B-e32f6e9-vs-3.12.0.md)
- [📈time plot](bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6%2B-e32f6e9-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.23x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6%2B-e32f6e9-vs-3.13.0b2.md)
- [📈time plot](bm-20240418-linux-x86_64-python-e32f6e9e4b202ce8759b-3.13.0a6%2B-e32f6e9-vs-3.13.0b2.svg)

