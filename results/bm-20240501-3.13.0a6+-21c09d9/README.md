# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [21c09d9](https://github.com/python/cpython/commit/21c09d9)
- commit date: 2024-05-01T01:33:28-07:00
- commit merge base: [fc7e1aa3c001bbce25973261fba457035719a559](https://github.com/python/cpython/commit/fc7e1aa3c001bbce25973261fba457035719a559)
- ref: 21c09d9f8195433f34b7

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8908365994)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6%2B-21c09d9.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.27x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6%2B-21c09d9-vs-3.10.4.md)
- [📈time plot](bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6%2B-21c09d9-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.97%, 1.01x faster at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6%2B-21c09d9-vs-3.12.0.md)
- [📈time plot](bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6%2B-21c09d9-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x faster (HPT: reliability of 99.82%, 1.00x faster at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6%2B-21c09d9-vs-3.13.0b2.md)
- [📈time plot](bm-20240501-linux-x86_64-python-21c09d9f8195433f34b7-3.13.0a6%2B-21c09d9-vs-3.13.0b2.svg)

