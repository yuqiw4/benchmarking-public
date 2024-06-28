# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [2770d5c](https://github.com/python/cpython/commit/2770d5c)
- commit date: 2024-05-02T08:55:29-07:00
- commit merge base: [72867c962cc59c6d56805f86530696bea6beb039](https://github.com/python/cpython/commit/72867c962cc59c6d56805f86530696bea6beb039)
- ref: main

## linux aarch64 (arminc)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8926888895)
- cpu model: missing
- platform: Linux-5.15.0-101-generic-aarch64-with-glibc2.35
- [raw results](bm-20240502-arminc-aarch64-python-main-3.13.0a6%2B-2770d5c.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.24x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240502-arminc-aarch64-python-main-3.13.0a6%2B-2770d5c-vs-3.10.4.md)
- [📈time plot](bm-20240502-arminc-aarch64-python-main-3.13.0a6%2B-2770d5c-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.95%, 1.00x faster at 99th %ile)
- Memory usage: 0.90x
- missing benchmarks: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240502-arminc-aarch64-python-main-3.13.0a6%2B-2770d5c-vs-3.12.0.md)
- [📈time plot](bm-20240502-arminc-aarch64-python-main-3.13.0a6%2B-2770d5c-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.02x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: aiohttp, bpe_tokeniser, flaskblogging, gunicorn, mypy2
- [📄table](bm-20240502-arminc-aarch64-python-main-3.13.0a6%2B-2770d5c-vs-3.13.0b2.md)
- [📈time plot](bm-20240502-arminc-aarch64-python-main-3.13.0a6%2B-2770d5c-vs-3.13.0b2.svg)

