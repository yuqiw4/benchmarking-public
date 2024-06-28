# Results

- fork: python
- version: 3.13.0a5+
- config: JIT
- commit hash: [6c8ac8a](https://github.com/python/cpython/commit/6c8ac8a)
- commit date: 2024-03-28T08:40:37+00:00
- commit merge base: [0f27672c5002de96c9f1228b12460d5ce3f1d190](https://github.com/python/cpython/commit/0f27672c5002de96c9f1228b12460d5ce3f1d190)
- ref: 6c8ac8a32fd6de196052

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8466063590)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240328-linux-x86_64-python-6c8ac8a32fd6de196052-3.13.0a5%2B-6c8ac8a.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240328-linux-x86_64-python-6c8ac8a32fd6de196052-3.13.0a5%2B-6c8ac8a-vs-3.10.4.md)
- [📈time plot](bm-20240328-linux-x86_64-python-6c8ac8a32fd6de196052-3.13.0a5%2B-6c8ac8a-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 75.63%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240328-linux-x86_64-python-6c8ac8a32fd6de196052-3.13.0a5%2B-6c8ac8a-vs-3.12.0.md)
- [📈time plot](bm-20240328-linux-x86_64-python-6c8ac8a32fd6de196052-3.13.0a5%2B-6c8ac8a-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 99.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: bpe_tokeniser, flaskblogging
- new benchmarks: unpack_sequence
- [📄table](bm-20240328-linux-x86_64-python-6c8ac8a32fd6de196052-3.13.0a5%2B-6c8ac8a-vs-3.13.0b2.md)
- [📈time plot](bm-20240328-linux-x86_64-python-6c8ac8a32fd6de196052-3.13.0a5%2B-6c8ac8a-vs-3.13.0b2.svg)

