# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: T2
- commit hash: [458d82f](https://github.com/faster%2dcpython/cpython/commit/458d82f)
- commit date: 2024-04-19T16:57:11+01:00
- commit merge base: [7e6fa5fceddc3f4721c036116c7a11533c8b23b3](https://github.com/faster%2dcpython/cpython/commit/7e6fa5fceddc3f4721c036116c7a11533c8b23b3)
- ref: convert_deopts_to_ex

## linux x86_64 (azure)

- [pystats raw](bm-20240419-azure-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f-pystats.json)
- [pystats table](bm-20240419-azure-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f-pystats.md)

### vs. base

- [pystats diff](bm-20240419-azure-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8756355892)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240419-linux-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f.json)

### vs. 3.10.4

- Geometric mean: 1.20x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240419-linux-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f-vs-3.10.4.md)
- [📈time plot](bm-20240419-linux-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.07x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 0.97x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240419-linux-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f-vs-3.12.0.md)
- [📈time plot](bm-20240419-linux-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.10x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240419-linux-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f-vs-3.13.0b2.md)
- [📈time plot](bm-20240419-linux-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240419-linux-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f-vs-base-mem.svg)
- [📄table](bm-20240419-linux-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f-vs-base.md)
- [📈time plot](bm-20240419-linux-x86_64-faster%252dcpython-convert_deopts_to_ex-3.13.0a6%2B-458d82f-vs-base.svg)

