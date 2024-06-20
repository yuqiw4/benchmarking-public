# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_funcs
- machine: linux-x86_64
- commit hash: b917d1f
- commit date: 2024-04-03
- overall geometric mean: 1.01x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 278 ms: 1.01x slower                                          |
| chameleon      | 7.22 ms                                                    | 6.92 ms: 1.04x faster                                         |
| docutils       | 2.83 sec                                                   | 2.89 sec: 1.02x slower                                        |
| html5lib       | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                         |
| tornado_http   | 94.6 ms                                                    | 97.0 ms: 1.03x slower                                         |
| Geometric mean | (ref)                                                      | 1.01x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|--------------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none_tg | 336 ms                                                     | 342 ms: 1.02x slower                                          |
| async_tree_none    | 378 ms                                                     | 390 ms: 1.03x slower                                          |
| Geometric mean     | (ref)                                                      | 1.00x slower                                                  |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.6 ms: 1.02x faster                                         |
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                          |
| nbody          | 88.3 ms                                                    | 92.8 ms: 1.05x slower                                         |
| Geometric mean | (ref)                                                      | 1.01x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.75 ms: 1.02x slower                                         |
| regex_v8       | 25.1 ms                                                    | 25.9 ms: 1.03x slower                                         |
| regex_dna      | 221 ms                                                     | 229 ms: 1.04x slower                                          |
| regex_compile  | 137 ms                                                     | 147 ms: 1.07x slower                                          |
| Geometric mean | (ref)                                                      | 1.04x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.14 us: 1.04x faster                                         |
| pickle_list          | 5.11 us                                                    | 5.00 us: 1.02x faster                                         |
| xml_etree_process    | 61.2 ms                                                    | 59.9 ms: 1.02x faster                                         |
| tomli_loads          | 2.12 sec                                                   | 2.08 sec: 1.02x faster                                        |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                         |
| json_loads           | 28.9 us                                                    | 28.4 us: 1.02x faster                                         |
| pickle_dict          | 34.8 us                                                    | 34.5 us: 1.01x faster                                         |
| pickle_pure_python   | 305 us                                                     | 307 us: 1.01x slower                                          |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                         |
| unpickle             | 15.1 us                                                    | 16.0 us: 1.06x slower                                         |
| unpickle_pure_python | 218 us                                                     | 239 us: 1.10x slower                                          |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                  |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_generate, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.04x slower                                         |
| python_startup_no_site | 7.11 ms                                                    | 9.57 ms: 1.35x slower                                         |
| Geometric mean         | (ref)                                                      | 1.18x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|-----------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                         |
| genshi_text     | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                         |
| django_template | 34.8 ms                                                    | 36.3 ms: 1.04x slower                                         |
| genshi_xml      | 51.6 ms                                                    | 55.3 ms: 1.07x slower                                         |
| Geometric mean  | (ref)                                                      | 1.02x slower                                                  |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|--------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 110 us: 1.49x faster                                          |
| scimark_fft              | 392 ms                                                     | 345 ms: 1.14x faster                                          |
| richards                 | 50.9 ms                                                    | 46.9 ms: 1.08x faster                                         |
| create_gc_cycles         | 1.82 ms                                                    | 1.69 ms: 1.07x faster                                         |
| richards_super           | 57.4 ms                                                    | 53.6 ms: 1.07x faster                                         |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.93 ms: 1.07x faster                                         |
| deepcopy_reduce          | 3.35 us                                                    | 3.16 us: 1.06x faster                                         |
| mdp                      | 2.79 sec                                                   | 2.66 sec: 1.05x faster                                        |
| mako                     | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                         |
| chameleon                | 7.22 ms                                                    | 6.92 ms: 1.04x faster                                         |
| crypto_pyaes             | 77.5 ms                                                    | 74.5 ms: 1.04x faster                                         |
| unpickle_list            | 5.34 us                                                    | 5.14 us: 1.04x faster                                         |
| coroutines               | 23.2 ms                                                    | 22.4 ms: 1.04x faster                                         |
| sqlite_synth             | 2.99 us                                                    | 2.89 us: 1.04x faster                                         |
| djangocms                | 31.5 us                                                    | 30.8 us: 1.02x faster                                         |
| pickle_list              | 5.11 us                                                    | 5.00 us: 1.02x faster                                         |
| xml_etree_process        | 61.2 ms                                                    | 59.9 ms: 1.02x faster                                         |
| tomli_loads              | 2.12 sec                                                   | 2.08 sec: 1.02x faster                                        |
| deepcopy                 | 367 us                                                     | 360 us: 1.02x faster                                          |
| json_dumps               | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                         |
| json_loads               | 28.9 us                                                    | 28.4 us: 1.02x faster                                         |
| pprint_pformat           | 1.56 sec                                                   | 1.53 sec: 1.02x faster                                        |
| float                    | 78.9 ms                                                    | 77.6 ms: 1.02x faster                                         |
| fannkuch                 | 402 ms                                                     | 396 ms: 1.01x faster                                          |
| deepcopy_memo            | 39.7 us                                                    | 39.1 us: 1.01x faster                                         |
| pickle_dict              | 34.8 us                                                    | 34.5 us: 1.01x faster                                         |
| gc_traversal             | 3.98 ms                                                    | 3.94 ms: 1.01x faster                                         |
| thrift                   | 823 us                                                     | 817 us: 1.01x faster                                          |
| pidigits                 | 191 ms                                                     | 190 ms: 1.01x faster                                          |
| asyncio_websockets       | 567 ms                                                     | 570 ms: 1.01x slower                                          |
| pickle_pure_python       | 305 us                                                     | 307 us: 1.01x slower                                          |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                        |
| bench_mp_pool            | 23.9 ms                                                    | 24.1 ms: 1.01x slower                                         |
| scimark_monte_carlo      | 69.2 ms                                                    | 69.8 ms: 1.01x slower                                         |
| meteor_contest           | 110 ms                                                     | 111 ms: 1.01x slower                                          |
| html5lib                 | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                         |
| json                     | 5.31 ms                                                    | 5.37 ms: 1.01x slower                                         |
| sqlglot_parse            | 1.32 ms                                                    | 1.34 ms: 1.01x slower                                         |
| sqlglot_transpile        | 1.63 ms                                                    | 1.66 ms: 1.01x slower                                         |
| 2to3                     | 274 ms                                                     | 278 ms: 1.01x slower                                          |
| generators               | 29.6 ms                                                    | 30.1 ms: 1.02x slower                                         |
| spectral_norm            | 116 ms                                                     | 118 ms: 1.02x slower                                          |
| async_tree_none_tg       | 336 ms                                                     | 342 ms: 1.02x slower                                          |
| docutils                 | 2.83 sec                                                   | 2.89 sec: 1.02x slower                                        |
| regex_effbot             | 3.67 ms                                                    | 3.75 ms: 1.02x slower                                         |
| gunicorn                 | 1.28 ms                                                    | 1.31 ms: 1.02x slower                                         |
| dask                     | 369 ms                                                     | 379 ms: 1.02x slower                                          |
| pickle                   | 11.5 us                                                    | 11.8 us: 1.03x slower                                         |
| tornado_http             | 94.6 ms                                                    | 97.0 ms: 1.03x slower                                         |
| bench_thread_pool        | 834 us                                                     | 855 us: 1.03x slower                                          |
| genshi_text              | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                         |
| sqlglot_normalize        | 110 ms                                                     | 113 ms: 1.03x slower                                          |
| chaos                    | 61.3 ms                                                    | 63.0 ms: 1.03x slower                                         |
| scimark_sor              | 127 ms                                                     | 131 ms: 1.03x slower                                          |
| aiohttp                  | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                         |
| sympy_str                | 282 ms                                                     | 290 ms: 1.03x slower                                          |
| regex_v8                 | 25.1 ms                                                    | 25.9 ms: 1.03x slower                                         |
| logging_format           | 6.47 us                                                    | 6.67 us: 1.03x slower                                         |
| async_tree_none          | 378 ms                                                     | 390 ms: 1.03x slower                                          |
| sympy_expand             | 473 ms                                                     | 489 ms: 1.03x slower                                          |
| python_startup           | 10.8 ms                                                    | 11.1 ms: 1.04x slower                                         |
| regex_dna                | 221 ms                                                     | 229 ms: 1.04x slower                                          |
| telco                    | 8.41 ms                                                    | 8.73 ms: 1.04x slower                                         |
| logging_simple           | 5.74 us                                                    | 5.97 us: 1.04x slower                                         |
| coverage                 | 93.1 ms                                                    | 97.0 ms: 1.04x slower                                         |
| sqlglot_optimize         | 55.5 ms                                                    | 57.9 ms: 1.04x slower                                         |
| async_generators         | 442 ms                                                     | 461 ms: 1.04x slower                                          |
| django_template          | 34.8 ms                                                    | 36.3 ms: 1.04x slower                                         |
| nbody                    | 88.3 ms                                                    | 92.8 ms: 1.05x slower                                         |
| dulwich_log              | 67.2 ms                                                    | 70.6 ms: 1.05x slower                                         |
| unpickle                 | 15.1 us                                                    | 16.0 us: 1.06x slower                                         |
| sympy_sum                | 156 ms                                                     | 165 ms: 1.06x slower                                          |
| mypy2                    | 742 ms                                                     | 787 ms: 1.06x slower                                          |
| pycparser                | 1.16 sec                                                   | 1.23 sec: 1.06x slower                                        |
| deltablue                | 3.25 ms                                                    | 3.47 ms: 1.07x slower                                         |
| sympy_integrate          | 20.5 ms                                                    | 21.9 ms: 1.07x slower                                         |
| genshi_xml               | 51.6 ms                                                    | 55.3 ms: 1.07x slower                                         |
| regex_compile            | 137 ms                                                     | 147 ms: 1.07x slower                                          |
| go                       | 145 ms                                                     | 157 ms: 1.09x slower                                          |
| scimark_lu               | 122 ms                                                     | 133 ms: 1.09x slower                                          |
| unpickle_pure_python     | 218 us                                                     | 239 us: 1.10x slower                                          |
| raytrace                 | 267 ms                                                     | 294 ms: 1.10x slower                                          |
| pathlib                  | 17.3 ms                                                    | 19.2 ms: 1.11x slower                                         |
| comprehensions           | 16.6 us                                                    | 18.5 us: 1.11x slower                                         |
| nqueens                  | 81.4 ms                                                    | 90.7 ms: 1.11x slower                                         |
| hexiom                   | 6.30 ms                                                    | 7.33 ms: 1.16x slower                                         |
| python_startup_no_site   | 7.11 ms                                                    | 9.57 ms: 1.35x slower                                         |
| Geometric mean           | (ref)                                                      | 1.01x slower                                                  |

Benchmark hidden because not significant (14): async_tree_cpu_io_mixed, async_tree_memoization, xml_etree_parse, async_tree_io_tg, logging_silent, async_tree_cpu_io_mixed_tg, pprint_safe_repr, xml_etree_generate, pyflate, asyncio_tcp, xml_etree_iterparse, async_tree_io, async_tree_memoization_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.05x