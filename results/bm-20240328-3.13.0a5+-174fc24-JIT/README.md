# Results

- fork: faster-cpython
- version: 3.13.0a5+
- config: JIT
- commit hash: [174fc24](https://github.com/faster%2dcpython/cpython/commit/174fc24)
- commit date: 2024-03-28T14:43:03+00:00
- commit merge base: [6c8ac8a32fd6de1960526561c44bc5603fab0f3e](https://github.com/faster%2dcpython/cpython/commit/6c8ac8a32fd6de1960526561c44bc5603fab0f3e)
- ref: no_thresholds

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8469090653)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240328-linux-x86_64-faster%252dcpython-no_thresholds-3.13.0a5%2B-174fc24.json)

### vs. 3.10.4

- Geometric mean: 1.27x faster (HPT: reliability of 100.00%, 1.19x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240328-linux-x86_64-faster%252dcpython-no_thresholds-3.13.0a5%2B-174fc24-vs-3.10.4.md)
- [📈time plot](bm-20240328-linux-x86_64-faster%252dcpython-no_thresholds-3.13.0a5%2B-174fc24-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.01x slower (HPT: reliability of 90.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240328-linux-x86_64-faster%252dcpython-no_thresholds-3.13.0a5%2B-174fc24-vs-3.12.0.md)
- [📈time plot](bm-20240328-linux-x86_64-faster%252dcpython-no_thresholds-3.13.0a5%2B-174fc24-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.04x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: bpe_tokeniser, flaskblogging
- new benchmarks: unpack_sequence
- [📄table](bm-20240328-linux-x86_64-faster%252dcpython-no_thresholds-3.13.0a5%2B-174fc24-vs-3.13.0b2.md)
- [📈time plot](bm-20240328-linux-x86_64-faster%252dcpython-no_thresholds-3.13.0a5%2B-174fc24-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.03x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240328-linux-x86_64-faster%252dcpython-no_thresholds-3.13.0a5%2B-174fc24-vs-base-mem.svg)
- [📄table](bm-20240328-linux-x86_64-faster%252dcpython-no_thresholds-3.13.0a5%2B-174fc24-vs-base.md)
- [📈time plot](bm-20240328-linux-x86_64-faster%252dcpython-no_thresholds-3.13.0a5%2B-174fc24-vs-base.svg)

