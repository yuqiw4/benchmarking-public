# Results

- fork: mdboom
- version: 3.13.0a5+
- config: JIT
- commit hash: [c35ee28](https://github.com/mdboom/cpython/commit/c35ee28)
- commit date: 2024-04-04T10:55:11-04:00
- commit merge base: [027fa2eccf39ddccdf7b416d16601277a7112054](https://github.com/mdboom/cpython/commit/027fa2eccf39ddccdf7b416d16601277a7112054)
- ref: dont_inline

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8559937355)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-3.10.4.md)
- [📈time plot](bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 81.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-3.12.0.md)
- [📈time plot](bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 99.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, django_template, djangocms, flaskblogging
- [📄table](bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-3.13.0b2.md)
- [📈time plot](bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 60.41%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-base-mem.svg)
- [📄table](bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-base.md)
- [📈time plot](bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-base.svg)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8556788888)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28.json)

### vs. 3.10.4

- Geometric mean: 1.26x faster (HPT: reliability of 100.00%, 1.17x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-3.10.4.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.03x slower (HPT: reliability of 99.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-3.12.0.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.02x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, django_template, flaskblogging
- [📄table](bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-3.13.0b2.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 71.31%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-base-mem.svg)
- [📄table](bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-base.md)
- [📈time plot](bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5%2B-c35ee28-vs-base.svg)

