# Results

- fork: python
- version: 3.13.0a5+
- config: JIT
- commit hash: [e569f91](https://github.com/python/cpython/commit/e569f91)
- commit date: 2024-04-02T16:08:16+02:00
- commit merge base: [52f5b7f9e05fc4a25e385c046e0b091641674556](https://github.com/python/cpython/commit/52f5b7f9e05fc4a25e385c046e0b091641674556)
- ref: e569f9132b5bdc1c1031

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8525964938)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5%2B-e569f91.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5%2B-e569f91-vs-3.10.4.md)
- [📈time plot](bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5%2B-e569f91-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 90.81%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5%2B-e569f91-vs-3.12.0.md)
- [📈time plot](bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5%2B-e569f91-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 99.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, django_template, djangocms, flaskblogging
- new benchmarks: unpack_sequence
- [📄table](bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5%2B-e569f91-vs-3.13.0b2.md)
- [📈time plot](bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5%2B-e569f91-vs-3.13.0b2.svg)

