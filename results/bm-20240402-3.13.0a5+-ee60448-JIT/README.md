# Results

- fork: mdboom
- version: 3.13.0a5+
- config: JIT
- commit hash: [ee60448](https://github.com/mdboom/cpython/commit/ee60448)
- commit date: 2024-04-02T14:25:50-04:00
- commit merge base: [027fa2eccf39ddccdf7b416d16601277a7112054](https://github.com/mdboom/cpython/commit/027fa2eccf39ddccdf7b416d16601277a7112054)
- ref: tier2_pystats_misses

## linux x86_64 (azure)

- [pystats raw](bm-20240402-azure-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-pystats.json)
- [pystats table](bm-20240402-azure-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-pystats.md)

## linux x86_64 (pythonperf2)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8540957831)
- cpu model: 12th Gen Intel(R) Core(TM) i9-12900
- platform: Linux-5.15.0-97-generic-x86_64-with-glibc2.35
- [raw results](bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448.json)

### vs. 3.10.4

- Geometric mean: 1.25x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-3.10.4.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.03x slower (HPT: reliability of 99.88%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-3.12.0.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, django_template, flaskblogging
- [📄table](bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-3.13.0b2.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 96.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-base-mem.svg)
- [📄table](bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-base.md)
- [📈time plot](bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5%2B-ee60448-vs-base.svg)

