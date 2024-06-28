# Results

- fork: python
- version: 3.13.0a6+
- config: JIT
- commit hash: [a74f117](https://github.com/python/cpython/commit/a74f117)
- commit date: 2024-04-14T00:08:03+01:00
- commit merge base: [3095d026424f11714f0b7a828c61dc741d4e716b](https://github.com/python/cpython/commit/3095d026424f11714f0b7a828c61dc741d4e716b)
- ref: a74f117dab369e6c5415

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8677067667)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240414-linux-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117.json)

### vs. 3.10.4

- Geometric mean: 1.32x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240414-linux-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.10.4.md)
- [📈time plot](bm-20240414-linux-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 84.97%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240414-linux-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.12.0.md)
- [📈time plot](bm-20240414-linux-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.00x slower (HPT: reliability of 99.95%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, django_template, djangocms, flaskblogging
- [📄table](bm-20240414-linux-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.13.0b2.md)
- [📈time plot](bm-20240414-linux-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.02x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- [🧠memory plot](bm-20240414-linux-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base-mem.svg)
- [📄table](bm-20240414-linux-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base.md)
- [📈time plot](bm-20240414-linux-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base.svg)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8677067667)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240414-pythonperf2-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117.json)

### vs. 3.10.4

- Geometric mean: 1.27x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240414-pythonperf2-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.10.4.md)
- [📈time plot](bm-20240414-pythonperf2-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.02x slower (HPT: reliability of 99.29%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240414-pythonperf2-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.12.0.md)
- [📈time plot](bm-20240414-pythonperf2-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, django_template, flaskblogging
- [📄table](bm-20240414-pythonperf2-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.13.0b2.md)
- [📈time plot](bm-20240414-pythonperf2-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.08x
- [🧠memory plot](bm-20240414-pythonperf2-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base-mem.svg)
- [📄table](bm-20240414-pythonperf2-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base.md)
- [📈time plot](bm-20240414-pythonperf2-x86_64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base.svg)

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8677067667)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.10.4.md)
- [📈time plot](bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.07x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.12.0.md)
- [📈time plot](bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 99.96%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: django_template, flaskblogging
- [📄table](bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.13.0b2.md)
- [📈time plot](bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 96.36%, 1.00x faster at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base.md)
- [📈time plot](bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base.svg)

## windows x86 (pythonperf1_win32)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8677067667)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117.json)

### vs. 3.10.4

- Geometric mean: 1.07x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.10.4.md)
- [📈time plot](bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.11x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.12.0.md)
- [📈time plot](bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.07x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: django_template, flaskblogging
- [📄table](bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.13.0b2.md)
- [📈time plot](bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.09x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: unknown
- [📄table](bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base.md)
- [📈time plot](bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base.svg)

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8677067667)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240414-darwin-arm64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117.json)

### vs. 3.10.4

- Geometric mean: 1.23x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240414-darwin-arm64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.10.4.md)
- [📈time plot](bm-20240414-darwin-arm64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.58%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240414-darwin-arm64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.12.0.md)
- [📈time plot](bm-20240414-darwin-arm64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.04x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: bpe_tokeniser, django_template, flaskblogging
- [📄table](bm-20240414-darwin-arm64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.13.0b2.md)
- [📈time plot](bm-20240414-darwin-arm64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.02x slower (HPT: reliability of 98.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20240414-darwin-arm64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base-mem.svg)
- [📄table](bm-20240414-darwin-arm64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base.md)
- [📈time plot](bm-20240414-darwin-arm64-python-a74f117dab369e6c5415-3.13.0a6%2B-a74f117-vs-base.svg)

