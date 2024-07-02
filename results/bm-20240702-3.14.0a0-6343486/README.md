# Results

- fork: python
- version: 3.14.0a0
- config: 
- commit hash: [6343486](https://github.com/python/cpython/commit/6343486)
- commit date: 2024-07-02T16:27:51+05:30
- commit merge base: [15232a0819a2f7e0f448f28f2e6081912d10e7cb](https://github.com/python/cpython/commit/15232a0819a2f7e0f448f28f2e6081912d10e7cb)
- ref: 6343486eb60ac5a9e154

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9764247137)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240702-pythonperf1-amd64-python-6343486eb60ac5a9e154-3.14.0a0-6343486.json)

### vs. 3.10.4

- Geometric mean: 1.20x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlite_synth, unpack_sequence, unpickle, unpickle_list
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240702-pythonperf1-amd64-python-6343486eb60ac5a9e154-3.14.0a0-6343486-vs-3.10.4.md)
- [📈time plot](bm-20240702-pythonperf1-amd64-python-6343486eb60ac5a9e154-3.14.0a0-6343486-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.01x faster (HPT: reliability of 80.47%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlite_synth, unpack_sequence, unpickle, unpickle_list
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240702-pythonperf1-amd64-python-6343486eb60ac5a9e154-3.14.0a0-6343486-vs-3.12.0.md)
- [📈time plot](bm-20240702-pythonperf1-amd64-python-6343486eb60ac5a9e154-3.14.0a0-6343486-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.04x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, chameleon, dulwich_log, flaskblogging, mypy2, pickle, pickle_dict, pickle_list, sqlite_synth, unpickle, unpickle_list
- [📄table](bm-20240702-pythonperf1-amd64-python-6343486eb60ac5a9e154-3.14.0a0-6343486-vs-3.13.0b2.md)
- [📈time plot](bm-20240702-pythonperf1-amd64-python-6343486eb60ac5a9e154-3.14.0a0-6343486-vs-3.13.0b2.svg)

