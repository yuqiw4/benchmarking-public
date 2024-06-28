# Results

- fork: python
- version: 3.13.0a6+
- config: JIT
- commit hash: [c408c36](https://github.com/python/cpython/commit/c408c36)
- commit date: 2024-05-01T17:58:22-04:00
- commit merge base: [a7711a2a4e5cf16b34fc284085da724a8c2c06dd](https://github.com/python/cpython/commit/a7711a2a4e5cf16b34fc284085da724a8c2c06dd)
- ref: c408c36e9b346f9f15a3

## linux aarch64 (arminc)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8931584972)
- cpu model: missing
- platform: Linux-5.15.0-101-generic-aarch64-with-glibc2.35
- [raw results](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36.json)

### vs. 3.10.4

- Geometric mean: 1.21x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.10.4.md)
- [📈time plot](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.05x slower (HPT: reliability of 99.99%, 1.01x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.12.0.md)
- [📈time plot](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.06x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: aiohttp, bpe_tokeniser, flaskblogging, gunicorn, mypy2
- [📄table](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.13.0b2.md)
- [📈time plot](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 81.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-base-mem.svg)
- [📄table](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-base.md)
- [📈time plot](bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-base.svg)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8933042107)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.10.4.md)
- [📈time plot](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 96.36%, 1.00x faster at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.12.0.md)
- [📈time plot](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.00x faster (HPT: reliability of 93.81%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.13.0b2.md)
- [📈time plot](bm-20240501-linux-x86_64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.13.0b2.svg)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8931577407)
- cpu model: missing
- platform: macOS-14.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.10.4.md)
- [📈time plot](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.12.0.md)
- [📈time plot](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.04x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.13.0b2.md)
- [📈time plot](bm-20240501-darwin-arm64-python-c408c36e9b346f9f15a3-3.13.0a6%2B-c408c36-vs-3.13.0b2.svg)

