# Results

- fork: python
- version: 3.13.0a5+
- config: JIT
- commit hash: [dcaf33a](https://github.com/python/cpython/commit/dcaf33a)
- commit date: 2024-03-20T17:33:08+01:00
- commit merge base: [44fbab43d8f3f2df07091d237824cf4fa1f6c57c](https://github.com/python/cpython/commit/44fbab43d8f3f2df07091d237824cf4fa1f6c57c)
- ref: dcaf33a41d5d220523d7

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8381067358)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240320-linux-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a.json)

### vs. 3.10.4

- Geometric mean: 1.13x faster (HPT: reliability of 99.99%, 1.07x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240320-linux-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.10.4.md)
- [📈time plot](bm-20240320-linux-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.25x slower (HPT: reliability of 99.98%, 1.01x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240320-linux-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.12.0.md)
- [📈time plot](bm-20240320-linux-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.28x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: bpe_tokeniser, flaskblogging
- new benchmarks: unpack_sequence
- [📄table](bm-20240320-linux-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.13.0b2.md)
- [📈time plot](bm-20240320-linux-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.13.0b2.svg)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8381067358)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a.json)

### vs. 3.10.4

- Geometric mean: 1.09x faster (HPT: reliability of 99.98%, 1.06x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.10.4.md)
- [📈time plot](bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.27x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.12.0.md)
- [📈time plot](bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.27x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: bpe_tokeniser, flaskblogging
- new benchmarks: unpack_sequence
- [📄table](bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.13.0b2.md)
- [📈time plot](bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.13.0b2.svg)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8381067358)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a.json)

### vs. 3.10.4

- Geometric mean: 1.06x faster (HPT: reliability of 99.98%, 1.07x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.10.4.md)
- [📈time plot](bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.17x slower (HPT: reliability of 64.01%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.12.0.md)
- [📈time plot](bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.27x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: flaskblogging
- new benchmarks: unpack_sequence
- [📄table](bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.13.0b2.md)
- [📈time plot](bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.13.0b2.svg)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8381067358)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a.json)

### vs. 3.10.4

- Geometric mean: 1.04x slower (HPT: reliability of 62.60%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.10.4.md)
- [📈time plot](bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.07x slower (HPT: reliability of 98.14%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.12.0.md)
- [📈time plot](bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.28x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: flaskblogging
- new benchmarks: unpack_sequence
- [📄table](bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.13.0b2.md)
- [📈time plot](bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.13.0b2.svg)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8381067358)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a.json)

### vs. 3.10.4

- Geometric mean: 1.03x faster (HPT: reliability of 99.51%, 1.00x faster at 99th %ile)
- Memory usage: 1.58x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.10.4.md)
- [📈time plot](bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.26x slower (HPT: reliability of 99.88%, 1.01x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.12.0.md)
- [📈time plot](bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.43x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: bpe_tokeniser, flaskblogging
- new benchmarks: unpack_sequence
- [📄table](bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.13.0b2.md)
- [📈time plot](bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5%2B-dcaf33a-vs-3.13.0b2.svg)

