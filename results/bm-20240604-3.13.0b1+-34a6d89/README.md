# Results

- fork: python
- version: 3.13.0b1+
- config: 
- commit hash: [34a6d89](https://github.com/python/cpython/commit/34a6d89)
- commit date: 2024-06-04T10:56:06-04:00
- ref: 34a6d897883935f13fc2

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9370026704)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240604-linux-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240604-linux-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.10.4.md)
- [📈time plot](bm-20240604-linux-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240604-linux-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.12.0.md)
- [📈time plot](bm-20240604-linux-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: bpe_tokeniser
- [📄table](bm-20240604-linux-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.13.0b2.md)
- [📈time plot](bm-20240604-linux-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.13.0b2.svg)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9370026704)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240604-pythonperf2-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89.json)

### vs. 3.10.4

- Geometric mean: 1.28x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240604-pythonperf2-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.10.4.md)
- [📈time plot](bm-20240604-pythonperf2-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.00x slower (HPT: reliability of 52.71%, 1.00x faster at 99th %ile)
- Memory usage: 0.94x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240604-pythonperf2-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.12.0.md)
- [📈time plot](bm-20240604-pythonperf2-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.00x faster (HPT: reliability of 77.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: bpe_tokeniser
- [📄table](bm-20240604-pythonperf2-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.13.0b2.md)
- [📈time plot](bm-20240604-pythonperf2-x86_64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.13.0b2.svg)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9370026704)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240604-pythonperf1-amd64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89.json)

### vs. 3.10.4

- Geometric mean: 1.24x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240604-pythonperf1-amd64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.10.4.md)
- [📈time plot](bm-20240604-pythonperf1-amd64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.09x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240604-pythonperf1-amd64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.12.0.md)
- [📈time plot](bm-20240604-pythonperf1-amd64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x faster (HPT: reliability of 97.80%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240604-pythonperf1-amd64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.13.0b2.md)
- [📈time plot](bm-20240604-pythonperf1-amd64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.13.0b2.svg)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9370026704)
- cpu model: missing
- platform: macOS-14.5-arm64-arm-64bit-Mach-O
- [raw results](bm-20240604-darwin-arm64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89.json)

### vs. 3.10.4

- Geometric mean: 1.27x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 0.59x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240604-darwin-arm64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.10.4.md)
- [📈time plot](bm-20240604-darwin-arm64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.08x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 0.59x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240604-darwin-arm64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.12.0.md)
- [📈time plot](bm-20240604-darwin-arm64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.00x faster (HPT: reliability of 81.92%, 1.00x faster at 99th %ile)
- Memory usage: 0.35x
- missing benchmarks: bpe_tokeniser
- [📄table](bm-20240604-darwin-arm64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.13.0b2.md)
- [📈time plot](bm-20240604-darwin-arm64-python-34a6d897883935f13fc2-3.13.0b1%2B-34a6d89-vs-3.13.0b2.svg)

