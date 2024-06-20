# Results

- fork: gaogaotiantian
- version: 3.13.0a5+
- config: JIT
- commit hash: [a65be06](https://github.com/gaogaotiantian/cpython/commit/a65be06)
- commit date: 2024-03-27T11:31:57-07:00
- commit merge base: [262fb911ab7df8e890ebd0efb0773c3e0b5a757f](https://github.com/gaogaotiantian/cpython/commit/262fb911ab7df8e890ebd0efb0773c3e0b5a757f)
- ref: optimize_sys_settrac

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8474043440)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5%2B-a65be06.json)

### vs. 3.10.4

- Geometric mean: 1.30x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5%2B-a65be06-vs-3.10.4.md)
- [📈time plot](bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5%2B-a65be06-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 52.19%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5%2B-a65be06-vs-3.12.0.md)
- [📈time plot](bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5%2B-a65be06-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x slower (HPT: reliability of 99.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.05x
- missing benchmarks: bpe_tokeniser, flaskblogging
- new benchmarks: unpack_sequence
- [📄table](bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5%2B-a65be06-vs-3.13.0b2.md)
- [📈time plot](bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5%2B-a65be06-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.12%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5%2B-a65be06-vs-base-mem.svg)
- [📄table](bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5%2B-a65be06-vs-base.md)
- [📈time plot](bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5%2B-a65be06-vs-base.svg)

