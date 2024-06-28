# Results

- fork: python
- version: 3.13.0a6+
- config: JIT
- commit hash: [15fbd53](https://github.com/python/cpython/commit/15fbd53)
- commit date: 2024-04-20T17:46:52+01:00
- commit merge base: [d8f350309ded3130c43f0d2809dcb8ec13112320](https://github.com/python/cpython/commit/d8f350309ded3130c43f0d2809dcb8ec13112320)
- ref: 15fbd53ba96be4b6a5ab

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8768575136)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.md)
- [📈time plot](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 97.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.md)
- [📈time plot](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.00x faster (HPT: reliability of 95.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.13.0b2.md)
- [📈time plot](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 99.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- [🧠memory plot](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base-mem.svg)
- [📄table](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base.md)
- [📈time plot](bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base.svg)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8768575136)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53.json)

### vs. 3.10.4

- Geometric mean: 1.27x faster (HPT: reliability of 100.00%, 1.18x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.md)
- [📈time plot](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.01x slower (HPT: reliability of 97.77%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.md)
- [📈time plot](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.13.0b2.md)
- [📈time plot](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- [🧠memory plot](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base-mem.svg)
- [📄table](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base.md)
- [📈time plot](bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base.svg)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8768575136)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.md)
- [📈time plot](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.08x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.md)
- [📈time plot](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 76.69%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: flaskblogging
- [📄table](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.13.0b2.md)
- [📈time plot](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.03x faster (HPT: reliability of 99.85%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base.md)
- [📈time plot](bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base.svg)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8768575136)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53.json)

### vs. 3.10.4

- Geometric mean: 1.07x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.md)
- [📈time plot](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.11x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.md)
- [📈time plot](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.07x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: flaskblogging
- [📄table](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.13.0b2.md)
- [📈time plot](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.09x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base.md)
- [📈time plot](bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base.svg)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8768575136)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53.json)

### vs. 3.10.4

- Geometric mean: 1.24x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.md)
- [📈time plot](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.md)
- [📈time plot](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.13.0b2.md)
- [📈time plot](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 92.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base-mem.svg)
- [📄table](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base.md)
- [📈time plot](bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6%2B-15fbd53-vs-base.svg)

