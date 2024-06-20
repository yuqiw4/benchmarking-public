# Results vs. 3.13.0b2

- fork: python
- ref: main
- machine: linux-aarch64
- commit hash: 2770d5c
- commit date: 2024-05-02
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 305 ms                                                       | 298 ms: 1.02x faster                                     |
| chameleon      | 8.95 ms                                                      | 9.06 ms: 1.01x slower                                    |
| docutils       | 3.10 sec                                                     | 3.06 sec: 1.01x faster                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                             |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|--------------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_io_tg   | 1.27 sec                                                     | 1.19 sec: 1.07x faster                                   |
| async_tree_none_tg | 476 ms                                                       | 462 ms: 1.03x faster                                     |
| Geometric mean     | (ref)                                                        | 1.02x faster                                             |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| nbody          | 114 ms                                                       | 106 ms: 1.08x faster                                     |
| float          | 91.4 ms                                                      | 88.7 ms: 1.03x faster                                    |
| pidigits       | 234 ms                                                       | 233 ms: 1.01x faster                                     |
| Geometric mean | (ref)                                                        | 1.04x faster                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna      | 259 ms                                                       | 248 ms: 1.04x faster                                     |
| regex_effbot   | 4.98 ms                                                      | 4.86 ms: 1.02x faster                                    |
| regex_compile  | 128 ms                                                       | 127 ms: 1.01x faster                                     |
| Geometric mean | (ref)                                                        | 1.02x faster                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| unpickle_list        | 6.52 us                                                      | 6.25 us: 1.04x faster                                    |
| tomli_loads          | 2.57 sec                                                     | 2.49 sec: 1.03x faster                                   |
| xml_etree_parse      | 191 ms                                                       | 186 ms: 1.03x faster                                     |
| xml_etree_generate   | 114 ms                                                       | 111 ms: 1.03x faster                                     |
| pickle_pure_python   | 359 us                                                       | 350 us: 1.02x faster                                     |
| json_dumps           | 13.1 ms                                                      | 12.8 ms: 1.02x faster                                    |
| xml_etree_process    | 80.8 ms                                                      | 79.4 ms: 1.02x faster                                    |
| unpickle_pure_python | 251 us                                                       | 248 us: 1.01x faster                                     |
| json_loads           | 32.1 us                                                      | 31.9 us: 1.01x faster                                    |
| unpickle             | 19.8 us                                                      | 19.6 us: 1.01x faster                                    |
| pickle_dict          | 37.6 us                                                      | 37.9 us: 1.01x slower                                    |
| Geometric mean       | (ref)                                                        | 1.02x faster                                             |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 13.0 ms                                                      | 12.1 ms: 1.07x faster                                    |
| python_startup_no_site | 8.60 ms                                                      | 8.29 ms: 1.04x faster                                    |
| Geometric mean         | (ref)                                                        | 1.06x faster                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| django_template | 42.3 ms                                                      | 40.5 ms: 1.04x faster                                    |
| genshi_xml      | 60.4 ms                                                      | 59.8 ms: 1.01x faster                                    |
| Geometric mean  | (ref)                                                        | 1.02x faster                                             |

Benchmark hidden because not significant (2): genshi_text, mako

All benchmarks:
===============

| Benchmark                | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| asyncio_tcp              | 584 ms                                                       | 530 ms: 1.10x faster                                     |
| nbody                    | 114 ms                                                       | 106 ms: 1.08x faster                                     |
| python_startup           | 13.0 ms                                                      | 12.1 ms: 1.07x faster                                    |
| async_tree_io_tg         | 1.27 sec                                                     | 1.19 sec: 1.07x faster                                   |
| telco                    | 10.0 ms                                                      | 9.38 ms: 1.07x faster                                    |
| richards                 | 55.9 ms                                                      | 52.8 ms: 1.06x faster                                    |
| scimark_lu               | 141 ms                                                       | 134 ms: 1.05x faster                                     |
| richards_super           | 62.3 ms                                                      | 59.4 ms: 1.05x faster                                    |
| django_template          | 42.3 ms                                                      | 40.5 ms: 1.04x faster                                    |
| deepcopy_memo            | 50.8 us                                                      | 48.6 us: 1.04x faster                                    |
| unpickle_list            | 6.52 us                                                      | 6.25 us: 1.04x faster                                    |
| regex_dna                | 259 ms                                                       | 248 ms: 1.04x faster                                     |
| asyncio_tcp_ssl          | 2.21 sec                                                     | 2.12 sec: 1.04x faster                                   |
| sqlglot_parse            | 1.42 ms                                                      | 1.37 ms: 1.04x faster                                    |
| python_startup_no_site   | 8.60 ms                                                      | 8.29 ms: 1.04x faster                                    |
| logging_format           | 7.82 us                                                      | 7.56 us: 1.04x faster                                    |
| logging_simple           | 7.21 us                                                      | 6.97 us: 1.03x faster                                    |
| nqueens                  | 98.9 ms                                                      | 95.7 ms: 1.03x faster                                    |
| sqlite_synth             | 3.90 us                                                      | 3.78 us: 1.03x faster                                    |
| dulwich_log              | 58.5 ms                                                      | 56.7 ms: 1.03x faster                                    |
| tomli_loads              | 2.57 sec                                                     | 2.49 sec: 1.03x faster                                   |
| async_tree_none_tg       | 476 ms                                                       | 462 ms: 1.03x faster                                     |
| float                    | 91.4 ms                                                      | 88.7 ms: 1.03x faster                                    |
| xml_etree_parse          | 191 ms                                                       | 186 ms: 1.03x faster                                     |
| comprehensions           | 20.5 us                                                      | 19.9 us: 1.03x faster                                    |
| scimark_sor              | 159 ms                                                       | 155 ms: 1.03x faster                                     |
| thrift                   | 962 us                                                       | 936 us: 1.03x faster                                     |
| sqlglot_optimize         | 62.6 ms                                                      | 61.0 ms: 1.03x faster                                    |
| chaos                    | 68.3 ms                                                      | 66.5 ms: 1.03x faster                                    |
| xml_etree_generate       | 114 ms                                                       | 111 ms: 1.03x faster                                     |
| async_generators         | 488 ms                                                       | 476 ms: 1.03x faster                                     |
| pickle_pure_python       | 359 us                                                       | 350 us: 1.02x faster                                     |
| regex_effbot             | 4.98 ms                                                      | 4.86 ms: 1.02x faster                                    |
| 2to3                     | 305 ms                                                       | 298 ms: 1.02x faster                                     |
| pprint_pformat           | 1.93 sec                                                     | 1.89 sec: 1.02x faster                                   |
| json_dumps               | 13.1 ms                                                      | 12.8 ms: 1.02x faster                                    |
| raytrace                 | 297 ms                                                       | 291 ms: 1.02x faster                                     |
| scimark_monte_carlo      | 82.3 ms                                                      | 80.6 ms: 1.02x faster                                    |
| deltablue                | 3.88 ms                                                      | 3.80 ms: 1.02x faster                                    |
| spectral_norm            | 141 ms                                                       | 139 ms: 1.02x faster                                     |
| xml_etree_process        | 80.8 ms                                                      | 79.4 ms: 1.02x faster                                    |
| sqlglot_transpile        | 1.71 ms                                                      | 1.68 ms: 1.02x faster                                    |
| logging_silent           | 133 ns                                                       | 131 ns: 1.02x faster                                     |
| scimark_fft              | 445 ms                                                       | 438 ms: 1.02x faster                                     |
| deepcopy                 | 448 us                                                       | 442 us: 1.01x faster                                     |
| sympy_expand             | 457 ms                                                       | 451 ms: 1.01x faster                                     |
| typing_runtime_protocols | 193 us                                                       | 191 us: 1.01x faster                                     |
| gc_traversal             | 5.17 ms                                                      | 5.10 ms: 1.01x faster                                    |
| unpickle_pure_python     | 251 us                                                       | 248 us: 1.01x faster                                     |
| mdp                      | 3.33 sec                                                     | 3.29 sec: 1.01x faster                                   |
| scimark_sparse_mat_mult  | 6.55 ms                                                      | 6.47 ms: 1.01x faster                                    |
| docutils                 | 3.10 sec                                                     | 3.06 sec: 1.01x faster                                   |
| go                       | 161 ms                                                       | 159 ms: 1.01x faster                                     |
| bench_mp_pool            | 7.03 ms                                                      | 6.95 ms: 1.01x faster                                    |
| coroutines               | 29.0 ms                                                      | 28.7 ms: 1.01x faster                                    |
| regex_compile            | 128 ms                                                       | 127 ms: 1.01x faster                                     |
| pprint_safe_repr         | 933 ms                                                       | 923 ms: 1.01x faster                                     |
| genshi_xml               | 60.4 ms                                                      | 59.8 ms: 1.01x faster                                    |
| deepcopy_reduce          | 4.04 us                                                      | 4.00 us: 1.01x faster                                    |
| json_loads               | 32.1 us                                                      | 31.9 us: 1.01x faster                                    |
| sympy_str                | 265 ms                                                       | 264 ms: 1.01x faster                                     |
| unpickle                 | 19.8 us                                                      | 19.6 us: 1.01x faster                                    |
| pidigits                 | 234 ms                                                       | 233 ms: 1.01x faster                                     |
| generators               | 37.1 ms                                                      | 37.2 ms: 1.00x slower                                    |
| pickle_dict              | 37.6 us                                                      | 37.9 us: 1.01x slower                                    |
| chameleon                | 8.95 ms                                                      | 9.06 ms: 1.01x slower                                    |
| Geometric mean           | (ref)                                                        | 1.02x faster                                             |

Benchmark hidden because not significant (31): sqlglot_normalize, async_tree_memoization_tg, tornado_http, async_tree_none, async_tree_cpu_io_mixed, create_gc_cycles, pycparser, json, hexiom, html5lib, async_tree_io, async_tree_memoization, sympy_integrate, genshi_text, xml_etree_iterparse, pickle, pylint, pyflate, mako, meteor_contest, asyncio_websockets, bench_thread_pool, coverage, sympy_sum, pathlib, pickle_list, crypto_pyaes, regex_v8, dask, fannkuch, async_tree_cpu_io_mixed_tg
Ignored benchmarks (5) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17.json: aiohttp, bpe_tokeniser, flaskblogging, gunicorn, mypy2

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x