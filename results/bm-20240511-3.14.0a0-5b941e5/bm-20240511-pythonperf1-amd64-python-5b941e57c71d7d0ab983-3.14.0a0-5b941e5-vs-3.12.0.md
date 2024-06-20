# Results vs. 3.12.0

- fork: python
- ref: 5b941e57c71d7d0ab983
- machine: windows-amd64
- commit hash: 5b941e5
- commit date: 2024-05-11
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 209 ms: 1.04x faster                                                       |
| chameleon      | 4.98 ms                                                     | 4.74 ms: 1.05x faster                                                      |
| docutils       | 1.66 sec                                                    | 1.62 sec: 1.02x faster                                                     |
| tornado_http   | 89.5 ms                                                     | 82.5 ms: 1.08x faster                                                      |
| Geometric mean | (ref)                                                       | 1.05x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 206 ms: 1.38x faster                                                       |
| async_tree_memoization_tg  | 367 ms                                                      | 266 ms: 1.38x faster                                                       |
| async_tree_none            | 291 ms                                                      | 220 ms: 1.32x faster                                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 382 ms: 1.31x faster                                                       |
| async_tree_memoization     | 339 ms                                                      | 267 ms: 1.27x faster                                                       |
| async_tree_io_tg           | 771 ms                                                      | 607 ms: 1.27x faster                                                       |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 386 ms: 1.27x faster                                                       |
| async_tree_io              | 731 ms                                                      | 587 ms: 1.25x faster                                                       |
| Geometric mean             | (ref)                                                       | 1.31x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 48.8 ms: 1.16x faster                                                      |
| nbody          | 71.9 ms                                                     | 68.4 ms: 1.05x faster                                                      |
| pidigits       | 152 ms                                                      | 150 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                       | 1.07x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 87.5 ms                                                     | 77.4 ms: 1.13x faster                                                      |
| regex_dna      | 126 ms                                                      | 119 ms: 1.06x faster                                                       |
| regex_effbot   | 1.62 ms                                                     | 1.63 ms: 1.01x slower                                                      |
| regex_v8       | 14.2 ms                                                     | 15.5 ms: 1.09x slower                                                      |
| Geometric mean | (ref)                                                       | 1.02x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle_pure_python | 133 us                                                      | 119 us: 1.12x faster                                                       |
| pickle_pure_python   | 195 us                                                      | 177 us: 1.10x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 52.7 ms: 1.06x faster                                                      |
| xml_etree_iterparse  | 65.2 ms                                                     | 61.5 ms: 1.06x faster                                                      |
| xml_etree_process    | 37.7 ms                                                     | 36.3 ms: 1.04x faster                                                      |
| pickle               | 7.43 us                                                     | 7.17 us: 1.04x faster                                                      |
| xml_etree_parse      | 93.0 ms                                                     | 90.1 ms: 1.03x faster                                                      |
| json_dumps           | 5.70 ms                                                     | 5.53 ms: 1.03x faster                                                      |
| pickle_dict          | 18.4 us                                                     | 18.3 us: 1.00x faster                                                      |
| json_loads           | 13.9 us                                                     | 14.0 us: 1.01x slower                                                      |
| tomli_loads          | 1.37 sec                                                    | 1.38 sec: 1.01x slower                                                     |
| unpickle_list        | 2.75 us                                                     | 2.83 us: 1.03x slower                                                      |
| unpickle             | 8.18 us                                                     | 8.88 us: 1.08x slower                                                      |
| pickle_list          | 2.83 us                                                     | 3.11 us: 1.10x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 20.5 ms: 1.05x slower                                                      |
| python_startup_no_site | 16.2 ms                                                     | 17.1 ms: 1.05x slower                                                      |
| Geometric mean         | (ref)                                                       | 1.05x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 6.20 ms: 1.14x faster                                                      |
| django_template | 22.9 ms                                                     | 22.0 ms: 1.04x faster                                                      |
| Geometric mean  | (ref)                                                       | 1.09x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.50 sec: 1.39x faster                                                     |
| async_tree_none_tg         | 285 ms                                                      | 206 ms: 1.38x faster                                                       |
| async_tree_memoization_tg  | 367 ms                                                      | 266 ms: 1.38x faster                                                       |
| comprehensions             | 14.1 us                                                     | 10.3 us: 1.37x faster                                                      |
| async_tree_none            | 291 ms                                                      | 220 ms: 1.32x faster                                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 382 ms: 1.31x faster                                                       |
| async_tree_memoization     | 339 ms                                                      | 267 ms: 1.27x faster                                                       |
| async_tree_io_tg           | 771 ms                                                      | 607 ms: 1.27x faster                                                       |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 386 ms: 1.27x faster                                                       |
| async_tree_io              | 731 ms                                                      | 587 ms: 1.25x faster                                                       |
| generators                 | 22.5 ms                                                     | 19.1 ms: 1.18x faster                                                      |
| float                      | 56.8 ms                                                     | 48.8 ms: 1.16x faster                                                      |
| raytrace                   | 192 ms                                                      | 167 ms: 1.15x faster                                                       |
| logging_silent             | 60.5 ns                                                     | 52.9 ns: 1.14x faster                                                      |
| mako                       | 7.09 ms                                                     | 6.20 ms: 1.14x faster                                                      |
| chaos                      | 43.3 ms                                                     | 38.3 ms: 1.13x faster                                                      |
| regex_compile              | 87.5 ms                                                     | 77.4 ms: 1.13x faster                                                      |
| deltablue                  | 2.16 ms                                                     | 1.92 ms: 1.13x faster                                                      |
| go                         | 91.6 ms                                                     | 81.4 ms: 1.12x faster                                                      |
| coroutines                 | 14.3 ms                                                     | 12.8 ms: 1.12x faster                                                      |
| unpickle_pure_python       | 133 us                                                      | 119 us: 1.12x faster                                                       |
| hexiom                     | 4.10 ms                                                     | 3.68 ms: 1.11x faster                                                      |
| pickle_pure_python         | 195 us                                                      | 177 us: 1.10x faster                                                       |
| sympy_str                  | 175 ms                                                      | 160 ms: 1.09x faster                                                       |
| nqueens                    | 62.8 ms                                                     | 57.4 ms: 1.09x faster                                                      |
| deepcopy                   | 238 us                                                      | 218 us: 1.09x faster                                                       |
| pprint_safe_repr           | 513 ms                                                      | 471 ms: 1.09x faster                                                       |
| sqlite_synth               | 1.76 us                                                     | 1.62 us: 1.09x faster                                                      |
| pprint_pformat             | 1.05 sec                                                    | 963 ms: 1.09x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 82.5 ms: 1.08x faster                                                      |
| spectral_norm              | 66.9 ms                                                     | 62.1 ms: 1.08x faster                                                      |
| sympy_sum                  | 91.5 ms                                                     | 84.9 ms: 1.08x faster                                                      |
| logging_simple             | 6.28 us                                                     | 5.82 us: 1.08x faster                                                      |
| logging_format             | 6.72 us                                                     | 6.27 us: 1.07x faster                                                      |
| deepcopy_reduce            | 2.09 us                                                     | 1.96 us: 1.07x faster                                                      |
| sqlglot_normalize          | 187 ms                                                      | 175 ms: 1.07x faster                                                       |
| scimark_lu                 | 58.9 ms                                                     | 55.1 ms: 1.07x faster                                                      |
| sympy_integrate            | 13.0 ms                                                     | 12.2 ms: 1.06x faster                                                      |
| scimark_sor                | 78.8 ms                                                     | 74.1 ms: 1.06x faster                                                      |
| deepcopy_memo              | 23.7 us                                                     | 22.3 us: 1.06x faster                                                      |
| xml_etree_generate         | 55.8 ms                                                     | 52.7 ms: 1.06x faster                                                      |
| regex_dna                  | 126 ms                                                      | 119 ms: 1.06x faster                                                       |
| xml_etree_iterparse        | 65.2 ms                                                     | 61.5 ms: 1.06x faster                                                      |
| sqlglot_parse              | 804 us                                                      | 764 us: 1.05x faster                                                       |
| chameleon                  | 4.98 ms                                                     | 4.74 ms: 1.05x faster                                                      |
| nbody                      | 71.9 ms                                                     | 68.4 ms: 1.05x faster                                                      |
| sqlglot_transpile          | 1.02 ms                                                     | 973 us: 1.05x faster                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 41.7 ms: 1.05x faster                                                      |
| bench_thread_pool          | 857 us                                                      | 818 us: 1.05x faster                                                       |
| pyflate                    | 295 ms                                                      | 282 ms: 1.04x faster                                                       |
| 2to3                       | 218 ms                                                      | 209 ms: 1.04x faster                                                       |
| sympy_expand               | 284 ms                                                      | 272 ms: 1.04x faster                                                       |
| django_template            | 22.9 ms                                                     | 22.0 ms: 1.04x faster                                                      |
| async_generators           | 239 ms                                                      | 230 ms: 1.04x faster                                                       |
| xml_etree_process          | 37.7 ms                                                     | 36.3 ms: 1.04x faster                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 33.3 ms: 1.04x faster                                                      |
| pickle                     | 7.43 us                                                     | 7.17 us: 1.04x faster                                                      |
| xml_etree_parse            | 93.0 ms                                                     | 90.1 ms: 1.03x faster                                                      |
| meteor_contest             | 74.6 ms                                                     | 72.4 ms: 1.03x faster                                                      |
| richards                   | 28.4 ms                                                     | 27.5 ms: 1.03x faster                                                      |
| json_dumps                 | 5.70 ms                                                     | 5.53 ms: 1.03x faster                                                      |
| richards_super             | 32.1 ms                                                     | 31.3 ms: 1.03x faster                                                      |
| docutils                   | 1.66 sec                                                    | 1.62 sec: 1.02x faster                                                     |
| crypto_pyaes               | 48.5 ms                                                     | 47.5 ms: 1.02x faster                                                      |
| pidigits                   | 152 ms                                                      | 150 ms: 1.01x faster                                                       |
| scimark_fft                | 184 ms                                                      | 182 ms: 1.01x faster                                                       |
| pathlib                    | 80.5 ms                                                     | 79.9 ms: 1.01x faster                                                      |
| pickle_dict                | 18.4 us                                                     | 18.3 us: 1.00x faster                                                      |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.57 ms: 1.01x slower                                                      |
| bench_mp_pool              | 69.2 ms                                                     | 69.7 ms: 1.01x slower                                                      |
| regex_effbot               | 1.62 ms                                                     | 1.63 ms: 1.01x slower                                                      |
| json_loads                 | 13.9 us                                                     | 14.0 us: 1.01x slower                                                      |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                      |
| tomli_loads                | 1.37 sec                                                    | 1.38 sec: 1.01x slower                                                     |
| fannkuch                   | 247 ms                                                      | 251 ms: 1.02x slower                                                       |
| json                       | 3.05 ms                                                     | 3.13 ms: 1.03x slower                                                      |
| unpickle_list              | 2.75 us                                                     | 2.83 us: 1.03x slower                                                      |
| mdp                        | 1.37 sec                                                    | 1.43 sec: 1.04x slower                                                     |
| typing_runtime_protocols   | 95.1 us                                                     | 99.6 us: 1.05x slower                                                      |
| python_startup             | 19.5 ms                                                     | 20.5 ms: 1.05x slower                                                      |
| python_startup_no_site     | 16.2 ms                                                     | 17.1 ms: 1.05x slower                                                      |
| coverage                   | 40.8 ms                                                     | 43.2 ms: 1.06x slower                                                      |
| unpickle                   | 8.18 us                                                     | 8.88 us: 1.08x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 15.5 ms: 1.09x slower                                                      |
| pickle_list                | 2.83 us                                                     | 3.11 us: 1.10x slower                                                      |
| telco                      | 4.13 ms                                                     | 4.77 ms: 1.16x slower                                                      |
| asyncio_tcp                | 487 ms                                                      | 564 ms: 1.16x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 892 us: 1.19x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                               |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (7) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240511-3.14.0a0-5b941e5/bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5.json: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: unknown