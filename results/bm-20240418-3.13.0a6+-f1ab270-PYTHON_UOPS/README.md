# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: T2
- commit hash: [f1ab270](https://github.com/faster%2dcpython/cpython/commit/f1ab270)
- commit date: 2024-04-18T11:10:10+01:00
- commit merge base: [e32f6e9e4b202ce8759b201f7eafe4982c0eaa41](https://github.com/faster%2dcpython/cpython/commit/e32f6e9e4b202ce8759b201f7eafe4982c0eaa41)
- ref: more_tier2_binary_op

## linux x86_64 (azure)

- [pystats raw](bm-20240418-azure-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270-pystats.json)
- [pystats table](bm-20240418-azure-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270-pystats.md)

### vs. base

- [pystats diff](bm-20240418-azure-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8736177709)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240418-linux-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270.json)

### vs. 3.10.4

- Geometric mean: 1.08x faster (HPT: reliability of 88.48%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240418-linux-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270-vs-3.10.4.md)
- [📈time plot](bm-20240418-linux-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.20x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240418-linux-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270-vs-3.12.0.md)
- [📈time plot](bm-20240418-linux-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.23x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240418-linux-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270-vs-3.13.0b2.md)
- [📈time plot](bm-20240418-linux-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 99.94%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240418-linux-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270-vs-base-mem.svg)
- [📄table](bm-20240418-linux-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270-vs-base.md)
- [📈time plot](bm-20240418-linux-x86_64-faster%252dcpython-more_tier2_binary_op-3.13.0a6%2B-f1ab270-vs-base.svg)

