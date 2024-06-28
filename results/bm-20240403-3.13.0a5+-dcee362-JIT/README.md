# Results

- fork: gvanrossum
- version: 3.13.0a5+
- config: JIT
- commit hash: [dcee362](https://github.com/gvanrossum/cpython/commit/dcee362)
- commit date: 2024-04-03T13:17:19-07:00
- commit merge base: [c43f6a4dfaa1c1974141e2f7014a7f98ca3a3f93](https://github.com/gvanrossum/cpython/commit/c43f6a4dfaa1c1974141e2f7014a7f98ca3a3f93)
- ref: exp_backoff

## darwin arm64 (darwin)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8545305709)
- cpu model: missing
- platform: macOS-14.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362.json)

### vs. 3.10.4

- Geometric mean: 1.22x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-3.10.4.md)
- [📈time plot](bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 98.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-3.12.0.md)
- [📈time plot](bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.04x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: bpe_tokeniser, django_template, flaskblogging
- [📄table](bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-3.13.0b2.md)
- [📈time plot](bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 98.91%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-base-mem.svg)
- [📄table](bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-base.md)
- [📈time plot](bm-20240403-darwin-arm64-gvanrossum-exp_backoff-3.13.0a5%2B-dcee362-vs-base.svg)

