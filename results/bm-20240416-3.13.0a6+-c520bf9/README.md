# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [c520bf9](https://github.com/python/cpython/commit/c520bf9)
- commit date: 2024-04-16T09:52:45+00:00
- commit merge base: [1316692e8c7c1e1f3b6639e51804f9db5ed892ea](https://github.com/python/cpython/commit/1316692e8c7c1e1f3b6639e51804f9db5ed892ea)
- ref: c520bf9bdf77d43c3d5d

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8708521791)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6%2B-c520bf9.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6%2B-c520bf9-vs-3.10.4.md)
- [📈time plot](bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6%2B-c520bf9-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.97%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6%2B-c520bf9-vs-3.12.0.md)
- [📈time plot](bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6%2B-c520bf9-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x faster (HPT: reliability of 91.63%, 1.00x faster at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6%2B-c520bf9-vs-3.13.0b2.md)
- [📈time plot](bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6%2B-c520bf9-vs-3.13.0b2.svg)

