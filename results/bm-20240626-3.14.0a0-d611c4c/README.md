# Results

- fork: python
- version: 3.14.0a0
- config: 
- commit hash: [d611c4c](https://github.com/python/cpython/commit/d611c4c)
- commit date: 2024-06-26T15:01:10-04:00
- commit merge base: [e51e880e75d79687b54a71351266e29ee349b4b8](https://github.com/python/cpython/commit/e51e880e75d79687b54a71351266e29ee349b4b8)
- ref: d611c4c8e9893c081696

## windows amd64 (pythonperf1)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/9748134543)
- cpu model: missing
- platform: Windows-11-10.0.22631-SP0
- [raw results](bm-20240626-pythonperf1-amd64-python-d611c4c8e9893c081696-3.14.0a0-d611c4c.json)

### vs. 3.10.4

- Geometric mean: 1.31x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlite_synth, unpack_sequence, unpickle, unpickle_list
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240626-pythonperf1-amd64-python-d611c4c8e9893c081696-3.14.0a0-d611c4c-vs-3.10.4.md)
- [📈time plot](bm-20240626-pythonperf1-amd64-python-d611c4c8e9893c081696-3.14.0a0-d611c4c-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.10x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlite_synth, unpack_sequence, unpickle, unpickle_list
- new benchmarks: genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240626-pythonperf1-amd64-python-d611c4c8e9893c081696-3.14.0a0-d611c4c-vs-3.12.0.md)
- [📈time plot](bm-20240626-pythonperf1-amd64-python-d611c4c8e9893c081696-3.14.0a0-d611c4c-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.05x faster (HPT: reliability of 57.21%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- missing benchmarks: aiohttp, chameleon, dulwich_log, flaskblogging, mypy2, pickle, pickle_dict, pickle_list, sqlite_synth, unpickle, unpickle_list
- [📄table](bm-20240626-pythonperf1-amd64-python-d611c4c8e9893c081696-3.14.0a0-d611c4c-vs-3.13.0b2.md)
- [📈time plot](bm-20240626-pythonperf1-amd64-python-d611c4c8e9893c081696-3.14.0a0-d611c4c-vs-3.13.0b2.svg)

