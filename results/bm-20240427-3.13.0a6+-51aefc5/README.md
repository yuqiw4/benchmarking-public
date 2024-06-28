# Results

- fork: python
- version: 3.13.0a6+
- config: 
- commit hash: [51aefc5](https://github.com/python/cpython/commit/51aefc5)
- commit date: 2024-04-27T11:36:06+01:00
- commit merge base: [c57326f48729f5cd7ddf7e2b38c4fd06d0962a41](https://github.com/python/cpython/commit/c57326f48729f5cd7ddf7e2b38c4fd06d0962a41)
- ref: 51aefc5bf907ddffaaf0

## linux x86_64 (azure)

- [pystats raw](bm-20240427-azure-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-pystats.json)
- [pystats table](bm-20240427-azure-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8863419643)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)
- [📈time plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.97%, 1.00x faster at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)
- [📈time plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x faster (HPT: reliability of 97.92%, 1.00x faster at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.13.0b2.md)
- [📈time plot](bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.13.0b2.svg)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8863419643)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5.json)

### vs. 3.10.4

- Geometric mean: 1.30x faster (HPT: reliability of 100.00%, 1.23x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)
- [📈time plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 83.84%, 1.00x faster at 99th %ile)
- Memory usage: 0.92x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)
- [📈time plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x faster (HPT: reliability of 98.91%, 1.00x faster at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.13.0b2.md)
- [📈time plot](bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.13.0b2.svg)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8863419643)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5.json)

### vs. 3.10.4

- Geometric mean: 1.19x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)
- [📈time plot](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)
- [📈time plot](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.04x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: flaskblogging
- [📄table](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.13.0b2.md)
- [📈time plot](bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.13.0b2.svg)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8863419643)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5.json)

### vs. 3.10.4

- Geometric mean: 1.16x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)
- [📈time plot](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.20x faster (HPT: reliability of 100.00%, 1.19x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)
- [📈time plot](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x faster (HPT: reliability of 97.02%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: flaskblogging
- [📄table](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.13.0b2.md)
- [📈time plot](bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.13.0b2.svg)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8863419643)
- cpu model: missing
- platform: macOS-14.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5.json)

### vs. 3.10.4

- Geometric mean: 1.24x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.md)
- [📈time plot](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.md)
- [📈time plot](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.13.0b2.md)
- [📈time plot](bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6%2B-51aefc5-vs-3.13.0b2.svg)

