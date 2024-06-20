# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 7819b1c
- commit date: 2024-05-03
- overall geometric mean: 1.01x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 270 ms: 1.01x faster                                                    |
| chameleon      | 7.22 ms                                                    | 6.96 ms: 1.04x faster                                                   |
| docutils       | 2.83 sec                                                   | 2.82 sec: 1.00x faster                                                  |
| tornado_http   | 94.6 ms                                                    | 94.1 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                      | 1.01x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 610 ms: 1.04x slower                                                    |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                            |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 85.7 ms: 1.03x faster                                                   |
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                      | 1.01x faster                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                    |
| regex_v8       | 25.1 ms                                                    | 25.9 ms: 1.03x slower                                                   |
| regex_dna      | 221 ms                                                     | 229 ms: 1.04x slower                                                    |
| regex_effbot   | 3.67 ms                                                    | 3.84 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                      | 1.02x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.6 us: 1.05x faster                                                   |
| unpickle_list        | 5.34 us                                                    | 5.14 us: 1.04x faster                                                   |
| xml_etree_parse      | 162 ms                                                     | 158 ms: 1.02x faster                                                    |
| xml_etree_iterparse  | 107 ms                                                     | 106 ms: 1.01x faster                                                    |
| unpickle_pure_python | 218 us                                                     | 216 us: 1.01x faster                                                    |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                   |
| xml_etree_generate   | 87.4 ms                                                    | 88.0 ms: 1.01x slower                                                   |
| tomli_loads          | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                  |
| pickle               | 11.5 us                                                    | 11.8 us: 1.02x slower                                                   |
| pickle_dict          | 34.8 us                                                    | 35.7 us: 1.03x slower                                                   |
| pickle_list          | 5.11 us                                                    | 5.32 us: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                            |

Benchmark hidden because not significant (3): pickle_pure_python, xml_etree_process, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                   |
| python_startup_no_site | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                   |
| genshi_text    | 23.7 ms                                                    | 23.2 ms: 1.02x faster                                                   |
| genshi_xml     | 51.6 ms                                                    | 50.9 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                      | 1.02x faster                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                                    |
| gc_traversal               | 3.98 ms                                                    | 3.74 ms: 1.06x faster                                                   |
| richards                   | 50.9 ms                                                    | 47.9 ms: 1.06x faster                                                   |
| richards_super             | 57.4 ms                                                    | 54.2 ms: 1.06x faster                                                   |
| scimark_fft                | 392 ms                                                     | 371 ms: 1.06x faster                                                    |
| scimark_lu                 | 122 ms                                                     | 116 ms: 1.05x faster                                                    |
| json_loads                 | 28.9 us                                                    | 27.6 us: 1.05x faster                                                   |
| crypto_pyaes               | 77.5 ms                                                    | 74.1 ms: 1.05x faster                                                   |
| mako                       | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                   |
| unpickle_list              | 5.34 us                                                    | 5.14 us: 1.04x faster                                                   |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                   |
| chameleon                  | 7.22 ms                                                    | 6.96 ms: 1.04x faster                                                   |
| deepcopy_memo              | 39.7 us                                                    | 38.5 us: 1.03x faster                                                   |
| nbody                      | 88.3 ms                                                    | 85.7 ms: 1.03x faster                                                   |
| logging_silent             | 105 ns                                                     | 102 ns: 1.03x faster                                                    |
| hexiom                     | 6.30 ms                                                    | 6.12 ms: 1.03x faster                                                   |
| nqueens                    | 81.4 ms                                                    | 79.3 ms: 1.03x faster                                                   |
| fannkuch                   | 402 ms                                                     | 392 ms: 1.03x faster                                                    |
| xml_etree_parse            | 162 ms                                                     | 158 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 3.35 us                                                    | 3.27 us: 1.02x faster                                                   |
| deepcopy                   | 367 us                                                     | 359 us: 1.02x faster                                                    |
| scimark_monte_carlo        | 69.2 ms                                                    | 67.6 ms: 1.02x faster                                                   |
| generators                 | 29.6 ms                                                    | 29.0 ms: 1.02x faster                                                   |
| sqlite_synth               | 2.99 us                                                    | 2.92 us: 1.02x faster                                                   |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.15 ms: 1.02x faster                                                   |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                   |
| logging_format             | 6.47 us                                                    | 6.34 us: 1.02x faster                                                   |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                    |
| genshi_text                | 23.7 ms                                                    | 23.2 ms: 1.02x faster                                                   |
| json                       | 5.31 ms                                                    | 5.21 ms: 1.02x faster                                                   |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                                   |
| pyflate                    | 484 ms                                                     | 477 ms: 1.01x faster                                                    |
| genshi_xml                 | 51.6 ms                                                    | 50.9 ms: 1.01x faster                                                   |
| pprint_pformat             | 1.56 sec                                                   | 1.54 sec: 1.01x faster                                                  |
| 2to3                       | 274 ms                                                     | 270 ms: 1.01x faster                                                    |
| xml_etree_iterparse        | 107 ms                                                     | 106 ms: 1.01x faster                                                    |
| sqlglot_parse              | 1.32 ms                                                    | 1.30 ms: 1.01x faster                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 54.8 ms: 1.01x faster                                                   |
| chaos                      | 61.3 ms                                                    | 60.6 ms: 1.01x faster                                                   |
| sqlglot_transpile          | 1.63 ms                                                    | 1.61 ms: 1.01x faster                                                   |
| mdp                        | 2.79 sec                                                   | 2.75 sec: 1.01x faster                                                  |
| sympy_str                  | 282 ms                                                     | 279 ms: 1.01x faster                                                    |
| unpickle_pure_python       | 218 us                                                     | 216 us: 1.01x faster                                                    |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                    |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                   |
| sympy_integrate            | 20.5 ms                                                    | 20.4 ms: 1.01x faster                                                   |
| pprint_safe_repr           | 758 ms                                                     | 753 ms: 1.01x faster                                                    |
| coverage                   | 93.1 ms                                                    | 92.5 ms: 1.01x faster                                                   |
| tornado_http               | 94.6 ms                                                    | 94.1 ms: 1.01x faster                                                   |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.01x faster                                                    |
| sqlglot_normalize          | 110 ms                                                     | 110 ms: 1.00x faster                                                    |
| comprehensions             | 16.6 us                                                    | 16.5 us: 1.00x faster                                                   |
| raytrace                   | 267 ms                                                     | 265 ms: 1.00x faster                                                    |
| docutils                   | 2.83 sec                                                   | 2.82 sec: 1.00x faster                                                  |
| asyncio_tcp                | 508 ms                                                     | 506 ms: 1.00x faster                                                    |
| bench_thread_pool          | 834 us                                                     | 831 us: 1.00x faster                                                    |
| python_startup_no_site     | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                                   |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x slower                                                  |
| pathlib                    | 17.3 ms                                                    | 17.4 ms: 1.00x slower                                                   |
| xml_etree_generate         | 87.4 ms                                                    | 88.0 ms: 1.01x slower                                                   |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                    |
| telco                      | 8.41 ms                                                    | 8.55 ms: 1.02x slower                                                   |
| djangocms                  | 31.5 us                                                    | 32.2 us: 1.02x slower                                                   |
| tomli_loads                | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                  |
| pickle                     | 11.5 us                                                    | 11.8 us: 1.02x slower                                                   |
| pickle_dict                | 34.8 us                                                    | 35.7 us: 1.03x slower                                                   |
| regex_v8                   | 25.1 ms                                                    | 25.9 ms: 1.03x slower                                                   |
| regex_dna                  | 221 ms                                                     | 229 ms: 1.04x slower                                                    |
| scimark_sor                | 127 ms                                                     | 132 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 610 ms: 1.04x slower                                                    |
| pycparser                  | 1.16 sec                                                   | 1.21 sec: 1.04x slower                                                  |
| pickle_list                | 5.11 us                                                    | 5.32 us: 1.04x slower                                                   |
| regex_effbot               | 3.67 ms                                                    | 3.84 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                            |

Benchmark hidden because not significant (29): async_tree_io, async_tree_memoization, flaskblogging, async_tree_memoization_tg, async_tree_none_tg, django_template, dask, mypy2, deltablue, html5lib, aiohttp, dulwich_log, go, pickle_pure_python, sympy_expand, async_generators, xml_etree_process, gunicorn, sympy_sum, spectral_norm, bench_mp_pool, unpickle, logging_simple, float, thrift, typing_runtime_protocols, pylint, async_tree_cpu_io_mixed, async_tree_io_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x