# Results

- fork: saulshanabrook
- version: 3.14.0a0
- config: JIT
- commit hash: [1520928](https://github.com/saulshanabrook/cpython/commit/1520928)
- commit date: 2024-05-20T16:55:29-04:00
- commit merge base: [642b25b9a82c368b045709f0b94e7d5a02400ed2](https://github.com/saulshanabrook/cpython/commit/642b25b9a82c368b045709f0b94e7d5a02400ed2)
- ref: optimzer_type_versio

## linux x86_64 (azure)

- [pystats raw](bm-20240520-azure-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928-pystats.json)
- [pystats table](bm-20240520-azure-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928-pystats.md)

### vs. base

- [pystats diff](bm-20240520-azure-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9165356177)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928.json)

### vs. 3.10.4

- Geometric mean: 1.33x faster (HPT: reliability of 100.00%, 1.24x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, djangocms, gunicorn, hexiom, mdp, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928-vs-3.10.4.md)
- [📈time plot](bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.04x faster (HPT: reliability of 97.20%, 1.00x faster at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: aiohttp, gunicorn, hexiom, mdp, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928-vs-3.12.0.md)
- [📈time plot](bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.00x faster (HPT: reliability of 89.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: aiohttp, bpe_tokeniser, djangocms, gunicorn, hexiom, mdp, mypy2
- [📄table](bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928-vs-3.13.0b2.md)
- [📈time plot](bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 62.77%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 hexiom, mdp
- [🧠memory plot](bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928-vs-base-mem.svg)
- [📄table](bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928-vs-base.md)
- [📈time plot](bm-20240520-linux-x86_64-saulshanabrook-optimzer_type_versio-3.14.0a0-1520928-vs-base.svg)

