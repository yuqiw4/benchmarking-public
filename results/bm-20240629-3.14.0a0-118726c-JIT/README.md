# Results

- fork: Fidget-Spinner
- version: 3.14.0a0
- config: JIT
- commit hash: [118726c](https://github.com/Fidget%2dSpinner/cpython/commit/118726c)
- commit date: 2024-06-29T02:42:16+08:00
- commit merge base: [e6543daf12051e9c660a5c0437683e8d2706a3c7](https://github.com/Fidget%2dSpinner/cpython/commit/e6543daf12051e9c660a5c0437683e8d2706a3c7)
- ref: optimizer_off

## linux x86_64 (azure)

- [pystats raw](bm-20240629-azure-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c-pystats.json)
- [pystats table](bm-20240629-azure-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c-pystats.md)

### vs. base

- [pystats diff](bm-20240629-azure-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c-pystats-vs-base.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9747898420)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-186-generic-x86_64-with-glibc2.31
- [raw results](bm-20240629-linux-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c.json)

### vs. 3.10.4

- Geometric mean: 1.41x faster (HPT: reliability of 100.00%, 1.25x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlite_synth, unpack_sequence, unpickle, unpickle_list
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, bpe_tokeniser
- [📄table](bm-20240629-linux-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c-vs-3.10.4.md)
- [📈time plot](bm-20240629-linux-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.07x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: aiohttp, chameleon, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlite_synth, unpack_sequence, unpickle, unpickle_list
- new benchmarks: bpe_tokeniser, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240629-linux-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c-vs-3.12.0.md)
- [📈time plot](bm-20240629-linux-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.04x faster (HPT: reliability of 99.92%, 1.01x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlite_synth, unpickle, unpickle_list
- [📄table](bm-20240629-linux-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c-vs-3.13.0b2.md)
- [📈time plot](bm-20240629-linux-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 99.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240629-linux-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c-vs-base-mem.svg)
- [📄table](bm-20240629-linux-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c-vs-base.md)
- [📈time plot](bm-20240629-linux-x86_64-Fidget%252dSpinner-optimizer_off-3.14.0a0-118726c-vs-base.svg)

