# Results

- fork: Fidget-Spinner
- version: 3.13.0a5+
- config: 
- commit hash: [4675ce8](https://github.com/Fidget%2dSpinner/cpython/commit/4675ce8)
- commit date: 2024-04-08T00:35:42+08:00
- commit merge base: [62aeb0ee69b06091396398de56dcb755ca3b9dc9](https://github.com/Fidget%2dSpinner/cpython/commit/62aeb0ee69b06091396398de56dcb755ca3b9dc9)
- ref: tagged_evaluation_st

## linux x86_64 (azure)

- [pystats raw](bm-20240408-azure-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-pystats.json)
- [pystats table](bm-20240408-azure-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-pystats.md)

### vs. base

- [pystats diff](bm-20240408-azure-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8591102155)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240408-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8.json)

### vs. 3.10.4

- Geometric mean: 1.35x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240408-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.10.4.md)
- [📈time plot](bm-20240408-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240408-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.12.0.md)
- [📈time plot](bm-20240408-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.02x faster (HPT: reliability of 99.98%, 1.00x faster at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: bpe_tokeniser, django_template, djangocms, flaskblogging
- [📄table](bm-20240408-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.13.0b2.md)
- [📈time plot](bm-20240408-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240408-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base-mem.svg)
- [📄table](bm-20240408-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base.md)
- [📈time plot](bm-20240408-linux-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base.svg)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8591102155)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240408-pythonperf2-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8.json)

### vs. 3.10.4

- Geometric mean: 1.30x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240408-pythonperf2-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.10.4.md)
- [📈time plot](bm-20240408-pythonperf2-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 62.50%, 1.00x faster at 99th %ile)
- Memory usage: 0.91x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240408-pythonperf2-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.12.0.md)
- [📈time plot](bm-20240408-pythonperf2-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x faster (HPT: reliability of 69.48%, 1.00x faster at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: bpe_tokeniser, django_template, flaskblogging
- [📄table](bm-20240408-pythonperf2-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.13.0b2.md)
- [📈time plot](bm-20240408-pythonperf2-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 99.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240408-pythonperf2-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base-mem.svg)
- [📄table](bm-20240408-pythonperf2-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base.md)
- [📈time plot](bm-20240408-pythonperf2-x86_64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base.svg)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8591102155)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240408-pythonperf1-amd64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8.json)

### vs. 3.10.4

- Geometric mean: 1.16x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240408-pythonperf1-amd64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.10.4.md)
- [📈time plot](bm-20240408-pythonperf1-amd64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 79.03%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240408-pythonperf1-amd64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.12.0.md)
- [📈time plot](bm-20240408-pythonperf1-amd64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.07x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: django_template, flaskblogging
- [📄table](bm-20240408-pythonperf1-amd64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.13.0b2.md)
- [📈time plot](bm-20240408-pythonperf1-amd64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.02x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240408-pythonperf1-amd64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base.md)
- [📈time plot](bm-20240408-pythonperf1-amd64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base.svg)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8591102155)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240408-pythonperf1_win32-x86-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8.json)

### vs. 3.10.4

- Geometric mean: 1.17x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240408-pythonperf1_win32-x86-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.10.4.md)
- [📈time plot](bm-20240408-pythonperf1_win32-x86-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.21x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240408-pythonperf1_win32-x86-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.12.0.md)
- [📈time plot](bm-20240408-pythonperf1_win32-x86-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.02x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: django_template, flaskblogging
- [📄table](bm-20240408-pythonperf1_win32-x86-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.13.0b2.md)
- [📈time plot](bm-20240408-pythonperf1_win32-x86-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 99.97%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240408-pythonperf1_win32-x86-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base.md)
- [📈time plot](bm-20240408-pythonperf1_win32-x86-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base.svg)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8591102155)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240408-darwin-arm64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8.json)

### vs. 3.10.4

- Geometric mean: 1.25x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240408-darwin-arm64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.10.4.md)
- [📈time plot](bm-20240408-darwin-arm64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.06x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240408-darwin-arm64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.12.0.md)
- [📈time plot](bm-20240408-darwin-arm64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.02x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: bpe_tokeniser, django_template, flaskblogging
- [📄table](bm-20240408-darwin-arm64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.13.0b2.md)
- [📈time plot](bm-20240408-darwin-arm64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240408-darwin-arm64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base-mem.svg)
- [📄table](bm-20240408-darwin-arm64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base.md)
- [📈time plot](bm-20240408-darwin-arm64-Fidget%252dSpinner-tagged_evaluation_st-3.13.0a5%2B-4675ce8-vs-base.svg)

