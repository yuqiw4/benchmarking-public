# Results

- fork: gvanrossum
- version: 3.13.0a5+
- config: T2
- commit hash: [7bb5618](https://github.com/gvanrossum/cpython/commit/7bb5618)
- commit date: 2024-03-29T13:30:17-07:00
- commit merge base: [94c97423a9c4969f8ddd4a3aa4aacb99c4d5263d](https://github.com/gvanrossum/cpython/commit/94c97423a9c4969f8ddd4a3aa4aacb99c4d5263d)
- ref: exp_backoff

## linux x86_64 (azure)

- [pystats raw](bm-20240329-azure-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618-pystats.json)
- [pystats table](bm-20240329-azure-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618-pystats.md)

### vs. base

- [pystats diff](bm-20240329-azure-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8485733184)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618.json)

### vs. 3.10.4

- Geometric mean: 1.15x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618-vs-3.10.4.md)
- [📈time plot](bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.12x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618-vs-3.12.0.md)
- [📈time plot](bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.14x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: bpe_tokeniser, flaskblogging
- new benchmarks: unpack_sequence
- [📄table](bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618-vs-3.13.0b2.md)
- [📈time plot](bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.08x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618-vs-base-mem.svg)
- [📄table](bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618-vs-base.md)
- [📈time plot](bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5%2B-7bb5618-vs-base.svg)

