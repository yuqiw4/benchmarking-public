# Results

- fork: python
- version: 3.13.0b2
- config: JIT
- commit hash: [3a83b17](https://github.com/python/cpython/commit/3a83b17)
- commit date: 2024-06-05T16:46:34+02:00
- ref: v3.13.0b2

## linux aarch64 (arminc)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9549289718)
- cpu model: missing
- platform: Linux-5.15.0-101-generic-aarch64-with-glibc2.35
- [raw results](bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17.json)

### vs. 3.10.4

- Geometric mean: 1.18x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, bpe_tokeniser
- [📄table](bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.10.4.md)
- [📈time plot](bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.07x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.12.0.md)
- [📈time plot](bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.09x
- [📄table](bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.13.0b2.md)
- [📈time plot](bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.09x
- [🧠memory plot](bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base-mem.svg)
- [📄table](bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base.md)
- [📈time plot](bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base.svg)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9549289718)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.22x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, bpe_tokeniser
- [📄table](bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.10.4.md)
- [📈time plot](bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 97.97%, 1.00x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: bpe_tokeniser, djangocms, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.12.0.md)
- [📈time plot](bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.00x faster (HPT: reliability of 57.69%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- [📄table](bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.13.0b2.md)
- [📈time plot](bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 57.69%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- [🧠memory plot](bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base-mem.svg)
- [📄table](bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base.md)
- [📈time plot](bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base.svg)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9549289718)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-105-generic-x86_64-with-glibc2.35
- [raw results](bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json)

### vs. 3.10.4

- Geometric mean: 1.27x faster (HPT: reliability of 100.00%, 1.19x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: docutils, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, bpe_tokeniser
- [📄table](bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.10.4.md)
- [📈time plot](bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.01x slower (HPT: reliability of 54.62%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: docutils, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: bpe_tokeniser, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.12.0.md)
- [📈time plot](bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.02x slower (HPT: reliability of 96.95%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: docutils
- [📄table](bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.13.0b2.md)
- [📈time plot](bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.02x slower (HPT: reliability of 96.95%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: 🔴 docutils
- [🧠memory plot](bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base-mem.svg)
- [📄table](bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base.md)
- [📈time plot](bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base.svg)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9549289718)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json)

### vs. 3.10.4

- Geometric mean: 1.19x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.10.4.md)
- [📈time plot](bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 99.23%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.12.0.md)
- [📈time plot](bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.04x slower (HPT: reliability of 99.91%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: sqlglot_normalize
- [📄table](bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.13.0b2.md)
- [📈time plot](bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.04x slower (HPT: reliability of 99.91%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: 🔴 sqlglot_normalize
- [📄table](bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base.md)
- [📈time plot](bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base.svg)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9549289718)
- cpu model: missing
- platform: macOS-14.5-arm64-arm-64bit-Mach-O
- [raw results](bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.18x faster at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, bpe_tokeniser
- [📄table](bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.10.4.md)
- [📈time plot](bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.05x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, bpe_tokeniser, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.12.0.md)
- [📈time plot](bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: sqlglot_normalize
- [📄table](bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.13.0b2.md)
- [📈time plot](bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: 🔴 sqlglot_normalize
- [🧠memory plot](bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base-mem.svg)
- [📄table](bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base.md)
- [📈time plot](bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17-vs-base.svg)

