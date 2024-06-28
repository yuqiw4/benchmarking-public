# Results

- fork: man-group
- version: 3.13.0a5+
- config: JIT
- commit hash: [9cf294a](https://github.com/man%2dgroup/cpython/commit/9cf294a)
- commit date: 2024-03-26T12:15:24+00:00
- commit merge base: [9654daf793b534b44a831c80f43505ab9e380f1f](https://github.com/man%2dgroup/cpython/commit/9654daf793b534b44a831c80f43505ab9e380f1f)
- ref: io_flush_full_buffer

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8738548223)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240326-linux-x86_64-man%252dgroup-io_flush_full_buffer-3.13.0a5%2B-9cf294a.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240326-linux-x86_64-man%252dgroup-io_flush_full_buffer-3.13.0a5%2B-9cf294a-vs-3.10.4.md)
- [📈time plot](bm-20240326-linux-x86_64-man%252dgroup-io_flush_full_buffer-3.13.0a5%2B-9cf294a-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.02x faster (HPT: reliability of 79.56%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240326-linux-x86_64-man%252dgroup-io_flush_full_buffer-3.13.0a5%2B-9cf294a-vs-3.12.0.md)
- [📈time plot](bm-20240326-linux-x86_64-man%252dgroup-io_flush_full_buffer-3.13.0a5%2B-9cf294a-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 97.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240326-linux-x86_64-man%252dgroup-io_flush_full_buffer-3.13.0a5%2B-9cf294a-vs-3.13.0b2.md)
- [📈time plot](bm-20240326-linux-x86_64-man%252dgroup-io_flush_full_buffer-3.13.0a5%2B-9cf294a-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 94.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240326-linux-x86_64-man%252dgroup-io_flush_full_buffer-3.13.0a5%2B-9cf294a-vs-base-mem.svg)
- [📄table](bm-20240326-linux-x86_64-man%252dgroup-io_flush_full_buffer-3.13.0a5%2B-9cf294a-vs-base.md)
- [📈time plot](bm-20240326-linux-x86_64-man%252dgroup-io_flush_full_buffer-3.13.0a5%2B-9cf294a-vs-base.svg)

