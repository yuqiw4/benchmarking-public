# Results vs. 3.13.0b2

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: linux-x86_64
- commit hash: d59145b
- commit date: 2024-04-26
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 267 ms: 1.03x faster                                                             |
| chameleon      | 7.22 ms                                                    | 7.06 ms: 1.02x faster                                                            |
| docutils       | 2.83 sec                                                   | 2.81 sec: 1.01x faster                                                           |
| html5lib       | 67.2 ms                                                    | 65.8 ms: 1.02x faster                                                            |
| tornado_http   | 94.6 ms                                                    | 93.8 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 351 ms: 1.08x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.8 ms: 1.01x faster                                                            |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                             |
| nbody          | 88.3 ms                                                    | 90.4 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.73 ms: 1.01x slower                                                            |
| regex_v8       | 25.1 ms                                                    | 25.7 ms: 1.02x slower                                                            |
| regex_dna      | 221 ms                                                     | 230 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.8 us: 1.04x faster                                                            |
| unpickle_pure_python | 218 us                                                     | 213 us: 1.02x faster                                                             |
| xml_etree_parse      | 162 ms                                                     | 158 ms: 1.02x faster                                                             |
| xml_etree_process    | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                            |
| pickle_pure_python   | 305 us                                                     | 300 us: 1.02x faster                                                             |
| pickle_list          | 5.11 us                                                    | 5.03 us: 1.02x faster                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 86.3 ms: 1.01x faster                                                            |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| pickle_dict          | 34.8 us                                                    | 35.9 us: 1.03x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.20 sec: 1.04x slower                                                           |
| pickle               | 11.5 us                                                    | 12.1 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (3): xml_etree_iterparse, unpickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 7.12 ms: 1.00x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 11.1 ms: 1.02x faster                                                            |
| genshi_text    | 23.7 ms                                                    | 23.8 ms: 1.01x slower                                                            |
| genshi_xml     | 51.6 ms                                                    | 52.1 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| richards                   | 50.9 ms                                                    | 46.0 ms: 1.11x faster                                                            |
| richards_super             | 57.4 ms                                                    | 52.5 ms: 1.09x faster                                                            |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.89 ms: 1.08x faster                                                            |
| async_tree_none            | 378 ms                                                     | 351 ms: 1.08x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                    | 3.13 us: 1.07x faster                                                            |
| logging_silent             | 105 ns                                                     | 98.0 ns: 1.07x faster                                                            |
| scimark_fft                | 392 ms                                                     | 371 ms: 1.06x faster                                                             |
| gc_traversal               | 3.98 ms                                                    | 3.78 ms: 1.05x faster                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 73.7 ms: 1.05x faster                                                            |
| scimark_sor                | 127 ms                                                     | 121 ms: 1.05x faster                                                             |
| deepcopy_memo              | 39.7 us                                                    | 37.9 us: 1.05x faster                                                            |
| go                         | 145 ms                                                     | 139 ms: 1.04x faster                                                             |
| json_loads                 | 28.9 us                                                    | 27.8 us: 1.04x faster                                                            |
| spectral_norm              | 116 ms                                                     | 112 ms: 1.04x faster                                                             |
| scimark_lu                 | 122 ms                                                     | 117 ms: 1.04x faster                                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.58 ms: 1.04x faster                                                            |
| raytrace                   | 267 ms                                                     | 257 ms: 1.04x faster                                                             |
| sqlglot_parse              | 1.32 ms                                                    | 1.27 ms: 1.04x faster                                                            |
| typing_runtime_protocols   | 165 us                                                     | 159 us: 1.04x faster                                                             |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                            |
| chaos                      | 61.3 ms                                                    | 59.4 ms: 1.03x faster                                                            |
| json                       | 5.31 ms                                                    | 5.15 ms: 1.03x faster                                                            |
| deepcopy                   | 367 us                                                     | 356 us: 1.03x faster                                                             |
| sympy_str                  | 282 ms                                                     | 274 ms: 1.03x faster                                                             |
| deltablue                  | 3.25 ms                                                    | 3.16 ms: 1.03x faster                                                            |
| coroutines                 | 23.2 ms                                                    | 22.6 ms: 1.03x faster                                                            |
| 2to3                       | 274 ms                                                     | 267 ms: 1.03x faster                                                             |
| unpickle_pure_python       | 218 us                                                     | 213 us: 1.02x faster                                                             |
| sympy_integrate            | 20.5 ms                                                    | 20.0 ms: 1.02x faster                                                            |
| pyflate                    | 484 ms                                                     | 474 ms: 1.02x faster                                                             |
| xml_etree_parse            | 162 ms                                                     | 158 ms: 1.02x faster                                                             |
| chameleon                  | 7.22 ms                                                    | 7.06 ms: 1.02x faster                                                            |
| sympy_expand               | 473 ms                                                     | 463 ms: 1.02x faster                                                             |
| html5lib                   | 67.2 ms                                                    | 65.8 ms: 1.02x faster                                                            |
| fannkuch                   | 402 ms                                                     | 394 ms: 1.02x faster                                                             |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 54.5 ms: 1.02x faster                                                            |
| xml_etree_process          | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                            |
| dulwich_log                | 67.2 ms                                                    | 65.9 ms: 1.02x faster                                                            |
| sqlite_synth               | 2.99 us                                                    | 2.94 us: 1.02x faster                                                            |
| pprint_pformat             | 1.56 sec                                                   | 1.53 sec: 1.02x faster                                                           |
| sympy_sum                  | 156 ms                                                     | 153 ms: 1.02x faster                                                             |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| pickle_pure_python         | 305 us                                                     | 300 us: 1.02x faster                                                             |
| aiohttp                    | 1.18 ms                                                    | 1.16 ms: 1.02x faster                                                            |
| logging_format             | 6.47 us                                                    | 6.36 us: 1.02x faster                                                            |
| mako                       | 11.2 ms                                                    | 11.1 ms: 1.02x faster                                                            |
| gunicorn                   | 1.28 ms                                                    | 1.26 ms: 1.02x faster                                                            |
| pickle_list                | 5.11 us                                                    | 5.03 us: 1.02x faster                                                            |
| sqlglot_normalize          | 110 ms                                                     | 109 ms: 1.01x faster                                                             |
| pprint_safe_repr           | 758 ms                                                     | 748 ms: 1.01x faster                                                             |
| float                      | 78.9 ms                                                    | 77.8 ms: 1.01x faster                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 86.3 ms: 1.01x faster                                                            |
| dask                       | 369 ms                                                     | 365 ms: 1.01x faster                                                             |
| generators                 | 29.6 ms                                                    | 29.3 ms: 1.01x faster                                                            |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| thrift                     | 823 us                                                     | 815 us: 1.01x faster                                                             |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                             |
| tornado_http               | 94.6 ms                                                    | 93.8 ms: 1.01x faster                                                            |
| mdp                        | 2.79 sec                                                   | 2.76 sec: 1.01x faster                                                           |
| nqueens                    | 81.4 ms                                                    | 80.7 ms: 1.01x faster                                                            |
| bench_thread_pool          | 834 us                                                     | 827 us: 1.01x faster                                                             |
| docutils                   | 2.83 sec                                                   | 2.81 sec: 1.01x faster                                                           |
| hexiom                     | 6.30 ms                                                    | 6.25 ms: 1.01x faster                                                            |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                             |
| python_startup_no_site     | 7.11 ms                                                    | 7.12 ms: 1.00x slower                                                            |
| genshi_text                | 23.7 ms                                                    | 23.8 ms: 1.01x slower                                                            |
| logging_simple             | 5.74 us                                                    | 5.78 us: 1.01x slower                                                            |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                             |
| genshi_xml                 | 51.6 ms                                                    | 52.1 ms: 1.01x slower                                                            |
| telco                      | 8.41 ms                                                    | 8.50 ms: 1.01x slower                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.73 ms: 1.01x slower                                                            |
| comprehensions             | 16.6 us                                                    | 17.0 us: 1.02x slower                                                            |
| regex_v8                   | 25.1 ms                                                    | 25.7 ms: 1.02x slower                                                            |
| nbody                      | 88.3 ms                                                    | 90.4 ms: 1.02x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 17.8 ms: 1.03x slower                                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                             |
| pickle_dict                | 34.8 us                                                    | 35.9 us: 1.03x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.20 sec: 1.03x slower                                                           |
| coverage                   | 93.1 ms                                                    | 96.5 ms: 1.04x slower                                                            |
| regex_dna                  | 221 ms                                                     | 230 ms: 1.04x slower                                                             |
| tomli_loads                | 2.12 sec                                                   | 2.20 sec: 1.04x slower                                                           |
| pickle                     | 11.5 us                                                    | 12.1 us: 1.05x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (18): async_tree_io, mypy2, pylint, async_tree_memoization_tg, async_tree_none_tg, xml_etree_iterparse, unpickle, async_tree_cpu_io_mixed, djangocms, async_tree_io_tg, asyncio_tcp_ssl, asyncio_tcp, unpickle_list, async_generators, scimark_monte_carlo, bench_mp_pool, django_template, async_tree_memoization
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x