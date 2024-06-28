# Results

- fork: mdboom
- version: 3.13.0a5+
- config: JIT
- commit hash: [81bda60](https://github.com/mdboom/cpython/commit/81bda60)
- commit date: 2024-04-05T10:30:13-04:00
- commit merge base: [687616877ba540a44f82ff764b5f13d36c0f3910](https://github.com/mdboom/cpython/commit/687616877ba540a44f82ff764b5f13d36c0f3910)
- ref: tier2_func_simple

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8571438753)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60.json)

### vs. 3.10.4

- Geometric mean: 1.32x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.10.4.md)
- [📈time plot](bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 86.56%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.12.0.md)
- [📈time plot](bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 99.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, django_template, djangocms, flaskblogging
- [📄table](bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.13.0b2.md)
- [📈time plot](bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 94.81%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base-mem.svg)
- [📄table](bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base.md)
- [📈time plot](bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base.svg)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8571438753)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60.json)

### vs. 3.10.4

- Geometric mean: 1.27x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.10.4.md)
- [📈time plot](bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.02x slower (HPT: reliability of 97.64%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.12.0.md)
- [📈time plot](bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 99.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: bpe_tokeniser, django_template, flaskblogging
- [📄table](bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.13.0b2.md)
- [📈time plot](bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 99.62%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base-mem.svg)
- [📄table](bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base.md)
- [📈time plot](bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base.svg)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8571438753)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.10.4.md)
- [📈time plot](bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.07x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.12.0.md)
- [📈time plot](bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 99.98%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: django_template, flaskblogging
- [📄table](bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.13.0b2.md)
- [📈time plot](bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 76.15%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base.md)
- [📈time plot](bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base.svg)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8571438753)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60.json)

### vs. 3.10.4

- Geometric mean: 1.06x faster (HPT: reliability of 99.97%, 1.01x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.10.4.md)
- [📈time plot](bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.10x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.12.0.md)
- [📈time plot](bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.08x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: django_template, flaskblogging
- [📄table](bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.13.0b2.md)
- [📈time plot](bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 97.80%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base.md)
- [📈time plot](bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base.svg)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8571438753)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.10.4.md)
- [📈time plot](bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.48%, 1.00x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.12.0.md)
- [📈time plot](bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.04x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: bpe_tokeniser, django_template, flaskblogging
- [📄table](bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.13.0b2.md)
- [📈time plot](bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base-mem.svg)
- [📄table](bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base.md)
- [📈time plot](bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5%2B-81bda60-vs-base.svg)

