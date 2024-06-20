# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.01x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 279 ms: 1.02x slower                                                |
| chameleon      | 7.22 ms                                                    | 7.07 ms: 1.02x faster                                               |
| docutils       | 2.83 sec                                                   | 2.94 sec: 1.04x slower                                              |
| html5lib       | 67.2 ms                                                    | 68.7 ms: 1.02x slower                                               |
| tornado_http   | 94.6 ms                                                    | 96.6 ms: 1.02x slower                                               |
| Geometric mean | (ref)                                                      | 1.02x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none | 378 ms                                                     | 354 ms: 1.07x faster                                                |
| Geometric mean  | (ref)                                                      | 1.01x faster                                                        |

Benchmark hidden because not significant (7): async_tree_memoization, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_io_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.0 ms: 1.02x faster                                               |
| pidigits       | 191 ms                                                     | 193 ms: 1.01x slower                                                |
| nbody          | 88.3 ms                                                    | 92.3 ms: 1.05x slower                                               |
| Geometric mean | (ref)                                                      | 1.01x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 25.5 ms: 1.02x slower                                               |
| regex_dna      | 221 ms                                                     | 230 ms: 1.04x slower                                                |
| regex_effbot   | 3.67 ms                                                    | 3.86 ms: 1.05x slower                                               |
| regex_compile  | 137 ms                                                     | 144 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                      | 1.04x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 2.03 sec: 1.05x faster                                              |
| unpickle_list        | 5.34 us                                                    | 5.12 us: 1.04x faster                                               |
| json_loads           | 28.9 us                                                    | 28.2 us: 1.02x faster                                               |
| pickle_list          | 5.11 us                                                    | 4.99 us: 1.02x faster                                               |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                               |
| pickle_dict          | 34.8 us                                                    | 34.1 us: 1.02x faster                                               |
| xml_etree_process    | 61.2 ms                                                    | 60.2 ms: 1.02x faster                                               |
| pickle_pure_python   | 305 us                                                     | 306 us: 1.00x slower                                                |
| xml_etree_generate   | 87.4 ms                                                    | 87.8 ms: 1.00x slower                                               |
| pickle               | 11.5 us                                                    | 11.6 us: 1.02x slower                                               |
| unpickle             | 15.1 us                                                    | 16.1 us: 1.06x slower                                               |
| unpickle_pure_python | 218 us                                                     | 241 us: 1.10x slower                                                |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                        |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                               |
| python_startup_no_site | 7.11 ms                                                    | 9.45 ms: 1.33x slower                                               |
| Geometric mean         | (ref)                                                      | 1.16x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                               |
| genshi_xml     | 51.6 ms                                                    | 54.1 ms: 1.05x slower                                               |
| genshi_text    | 23.7 ms                                                    | 25.2 ms: 1.06x slower                                               |
| Geometric mean | (ref)                                                      | 1.02x slower                                                        |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|--------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 114 us: 1.44x faster                                                |
| richards                 | 50.9 ms                                                    | 44.2 ms: 1.15x faster                                               |
| scimark_fft              | 392 ms                                                     | 341 ms: 1.15x faster                                                |
| richards_super           | 57.4 ms                                                    | 50.3 ms: 1.14x faster                                               |
| pylint                   | 317 ms                                                     | 295 ms: 1.07x faster                                                |
| async_tree_none          | 378 ms                                                     | 354 ms: 1.07x faster                                                |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.94 ms: 1.07x faster                                               |
| gc_traversal             | 3.98 ms                                                    | 3.77 ms: 1.05x faster                                               |
| create_gc_cycles         | 1.82 ms                                                    | 1.73 ms: 1.05x faster                                               |
| mako                     | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                               |
| tomli_loads              | 2.12 sec                                                   | 2.03 sec: 1.05x faster                                              |
| unpickle_list            | 5.34 us                                                    | 5.12 us: 1.04x faster                                               |
| sqlite_synth             | 2.99 us                                                    | 2.88 us: 1.04x faster                                               |
| pyflate                  | 484 ms                                                     | 468 ms: 1.03x faster                                                |
| deepcopy_reduce          | 3.35 us                                                    | 3.25 us: 1.03x faster                                               |
| float                    | 78.9 ms                                                    | 77.0 ms: 1.02x faster                                               |
| coroutines               | 23.2 ms                                                    | 22.6 ms: 1.02x faster                                               |
| json_loads               | 28.9 us                                                    | 28.2 us: 1.02x faster                                               |
| crypto_pyaes             | 77.5 ms                                                    | 75.6 ms: 1.02x faster                                               |
| pickle_list              | 5.11 us                                                    | 4.99 us: 1.02x faster                                               |
| json_dumps               | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                               |
| fannkuch                 | 402 ms                                                     | 393 ms: 1.02x faster                                                |
| chameleon                | 7.22 ms                                                    | 7.07 ms: 1.02x faster                                               |
| pickle_dict              | 34.8 us                                                    | 34.1 us: 1.02x faster                                               |
| deepcopy_memo            | 39.7 us                                                    | 39.0 us: 1.02x faster                                               |
| xml_etree_process        | 61.2 ms                                                    | 60.2 ms: 1.02x faster                                               |
| deepcopy                 | 367 us                                                     | 363 us: 1.01x faster                                                |
| logging_format           | 6.47 us                                                    | 6.42 us: 1.01x faster                                               |
| mdp                      | 2.79 sec                                                   | 2.77 sec: 1.01x faster                                              |
| pickle_pure_python       | 305 us                                                     | 306 us: 1.00x slower                                                |
| xml_etree_generate       | 87.4 ms                                                    | 87.8 ms: 1.00x slower                                               |
| pprint_safe_repr         | 758 ms                                                     | 762 ms: 1.01x slower                                                |
| sqlglot_parse            | 1.32 ms                                                    | 1.33 ms: 1.01x slower                                               |
| pidigits                 | 191 ms                                                     | 193 ms: 1.01x slower                                                |
| sqlglot_transpile        | 1.63 ms                                                    | 1.65 ms: 1.01x slower                                               |
| asyncio_tcp              | 508 ms                                                     | 513 ms: 1.01x slower                                                |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                              |
| json                     | 5.31 ms                                                    | 5.36 ms: 1.01x slower                                               |
| meteor_contest           | 110 ms                                                     | 111 ms: 1.01x slower                                                |
| generators               | 29.6 ms                                                    | 30.0 ms: 1.01x slower                                               |
| dask                     | 369 ms                                                     | 375 ms: 1.01x slower                                                |
| pickle                   | 11.5 us                                                    | 11.6 us: 1.02x slower                                               |
| logging_silent           | 105 ns                                                     | 106 ns: 1.02x slower                                                |
| logging_simple           | 5.74 us                                                    | 5.83 us: 1.02x slower                                               |
| regex_v8                 | 25.1 ms                                                    | 25.5 ms: 1.02x slower                                               |
| gunicorn                 | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                               |
| 2to3                     | 274 ms                                                     | 279 ms: 1.02x slower                                                |
| python_startup           | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                               |
| tornado_http             | 94.6 ms                                                    | 96.6 ms: 1.02x slower                                               |
| chaos                    | 61.3 ms                                                    | 62.6 ms: 1.02x slower                                               |
| html5lib                 | 67.2 ms                                                    | 68.7 ms: 1.02x slower                                               |
| scimark_monte_carlo      | 69.2 ms                                                    | 70.7 ms: 1.02x slower                                               |
| aiohttp                  | 1.18 ms                                                    | 1.21 ms: 1.02x slower                                               |
| pprint_pformat           | 1.56 sec                                                   | 1.59 sec: 1.03x slower                                              |
| bench_thread_pool        | 834 us                                                     | 857 us: 1.03x slower                                                |
| sqlglot_normalize        | 110 ms                                                     | 114 ms: 1.03x slower                                                |
| raytrace                 | 267 ms                                                     | 275 ms: 1.03x slower                                                |
| telco                    | 8.41 ms                                                    | 8.68 ms: 1.03x slower                                               |
| docutils                 | 2.83 sec                                                   | 2.94 sec: 1.04x slower                                              |
| sqlglot_optimize         | 55.5 ms                                                    | 57.6 ms: 1.04x slower                                               |
| regex_dna                | 221 ms                                                     | 230 ms: 1.04x slower                                                |
| async_generators         | 442 ms                                                     | 461 ms: 1.04x slower                                                |
| dulwich_log              | 67.2 ms                                                    | 70.1 ms: 1.04x slower                                               |
| nbody                    | 88.3 ms                                                    | 92.3 ms: 1.05x slower                                               |
| genshi_xml               | 51.6 ms                                                    | 54.1 ms: 1.05x slower                                               |
| sympy_expand             | 473 ms                                                     | 496 ms: 1.05x slower                                                |
| regex_effbot             | 3.67 ms                                                    | 3.86 ms: 1.05x slower                                               |
| pycparser                | 1.16 sec                                                   | 1.22 sec: 1.05x slower                                              |
| sympy_str                | 282 ms                                                     | 297 ms: 1.05x slower                                                |
| regex_compile            | 137 ms                                                     | 144 ms: 1.05x slower                                                |
| mypy2                    | 742 ms                                                     | 786 ms: 1.06x slower                                                |
| coverage                 | 93.1 ms                                                    | 98.9 ms: 1.06x slower                                               |
| genshi_text              | 23.7 ms                                                    | 25.2 ms: 1.06x slower                                               |
| unpickle                 | 15.1 us                                                    | 16.1 us: 1.06x slower                                               |
| go                       | 145 ms                                                     | 155 ms: 1.07x slower                                                |
| sympy_sum                | 156 ms                                                     | 168 ms: 1.08x slower                                                |
| comprehensions           | 16.6 us                                                    | 17.9 us: 1.08x slower                                               |
| sympy_integrate          | 20.5 ms                                                    | 22.1 ms: 1.08x slower                                               |
| scimark_lu               | 122 ms                                                     | 132 ms: 1.09x slower                                                |
| pathlib                  | 17.3 ms                                                    | 19.0 ms: 1.10x slower                                               |
| scimark_sor              | 127 ms                                                     | 140 ms: 1.10x slower                                                |
| unpickle_pure_python     | 218 us                                                     | 241 us: 1.10x slower                                                |
| nqueens                  | 81.4 ms                                                    | 90.5 ms: 1.11x slower                                               |
| hexiom                   | 6.30 ms                                                    | 7.01 ms: 1.11x slower                                               |
| deltablue                | 3.25 ms                                                    | 3.70 ms: 1.14x slower                                               |
| python_startup_no_site   | 7.11 ms                                                    | 9.45 ms: 1.33x slower                                               |
| Geometric mean           | (ref)                                                      | 1.01x slower                                                        |

Benchmark hidden because not significant (13): async_tree_memoization, spectral_norm, async_tree_cpu_io_mixed, async_tree_io, xml_etree_parse, async_tree_memoization_tg, asyncio_websockets, xml_etree_iterparse, async_tree_none_tg, bench_mp_pool, async_tree_io_tg, thrift, async_tree_cpu_io_mixed_tg
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x