# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: bfc2286
- commit date: 2024-04-17
- overall geometric mean: 1.01x faster
- HPT reliability: 94.45%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 272 ms: 1.01x faster                                                          |
| chameleon      | 7.22 ms                                                    | 7.12 ms: 1.01x faster                                                         |
| docutils       | 2.83 sec                                                   | 2.84 sec: 1.00x slower                                                        |
| html5lib       | 67.2 ms                                                    | 68.6 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                  |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none | 378 ms                                                     | 350 ms: 1.08x faster                                                          |
| async_tree_io   | 939 ms                                                     | 912 ms: 1.03x faster                                                          |
| Geometric mean  | (ref)                                                      | 1.02x faster                                                                  |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 84.7 ms: 1.04x faster                                                         |
| float          | 78.9 ms                                                    | 77.6 ms: 1.02x faster                                                         |
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 136 ms: 1.00x faster                                                          |
| regex_v8       | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                         |
| regex_dna      | 221 ms                                                     | 224 ms: 1.01x slower                                                          |
| regex_effbot   | 3.67 ms                                                    | 3.73 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.6 us: 1.05x faster                                                         |
| unpickle_list        | 5.34 us                                                    | 5.24 us: 1.02x faster                                                         |
| xml_etree_parse      | 162 ms                                                     | 159 ms: 1.02x faster                                                          |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                         |
| xml_etree_process    | 61.2 ms                                                    | 60.8 ms: 1.01x faster                                                         |
| xml_etree_generate   | 87.4 ms                                                    | 88.3 ms: 1.01x slower                                                         |
| unpickle_pure_python | 218 us                                                     | 222 us: 1.02x slower                                                          |
| unpickle             | 15.1 us                                                    | 15.5 us: 1.03x slower                                                         |
| pickle_dict          | 34.8 us                                                    | 36.0 us: 1.03x slower                                                         |
| pickle               | 11.5 us                                                    | 12.1 us: 1.05x slower                                                         |
| tomli_loads          | 2.12 sec                                                   | 2.24 sec: 1.06x slower                                                        |
| pickle_list          | 5.11 us                                                    | 5.41 us: 1.06x slower                                                         |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                                  |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                         |
| python_startup_no_site | 7.11 ms                                                    | 7.07 ms: 1.01x faster                                                         |
| Geometric mean         | (ref)                                                      | 1.02x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 11.1 ms: 1.01x faster                                                         |
| django_template | 34.8 ms                                                    | 35.1 ms: 1.01x slower                                                         |
| genshi_xml      | 51.6 ms                                                    | 52.1 ms: 1.01x slower                                                         |
| Geometric mean  | (ref)                                                      | 1.00x slower                                                                  |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|--------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 115 us: 1.43x faster                                                          |
| async_tree_none          | 378 ms                                                     | 350 ms: 1.08x faster                                                          |
| richards_super           | 57.4 ms                                                    | 54.0 ms: 1.06x faster                                                         |
| scimark_lu               | 122 ms                                                     | 115 ms: 1.06x faster                                                          |
| richards                 | 50.9 ms                                                    | 48.0 ms: 1.06x faster                                                         |
| gc_traversal             | 3.98 ms                                                    | 3.76 ms: 1.06x faster                                                         |
| json_loads               | 28.9 us                                                    | 27.6 us: 1.05x faster                                                         |
| scimark_fft              | 392 ms                                                     | 376 ms: 1.04x faster                                                          |
| nbody                    | 88.3 ms                                                    | 84.7 ms: 1.04x faster                                                         |
| create_gc_cycles         | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                         |
| crypto_pyaes             | 77.5 ms                                                    | 74.6 ms: 1.04x faster                                                         |
| deepcopy_memo            | 39.7 us                                                    | 38.3 us: 1.04x faster                                                         |
| deepcopy_reduce          | 3.35 us                                                    | 3.24 us: 1.03x faster                                                         |
| deepcopy                 | 367 us                                                     | 357 us: 1.03x faster                                                          |
| async_tree_io            | 939 ms                                                     | 912 ms: 1.03x faster                                                          |
| python_startup           | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                         |
| scimark_sor              | 127 ms                                                     | 125 ms: 1.02x faster                                                          |
| sqlite_synth             | 2.99 us                                                    | 2.93 us: 1.02x faster                                                         |
| unpickle_list            | 5.34 us                                                    | 5.24 us: 1.02x faster                                                         |
| sqlglot_transpile        | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                         |
| coroutines               | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                                         |
| sqlglot_parse            | 1.32 ms                                                    | 1.30 ms: 1.02x faster                                                         |
| float                    | 78.9 ms                                                    | 77.6 ms: 1.02x faster                                                         |
| chaos                    | 61.3 ms                                                    | 60.4 ms: 1.02x faster                                                         |
| xml_etree_parse          | 162 ms                                                     | 159 ms: 1.02x faster                                                          |
| thrift                   | 823 us                                                     | 810 us: 1.02x faster                                                          |
| mako                     | 11.2 ms                                                    | 11.1 ms: 1.01x faster                                                         |
| chameleon                | 7.22 ms                                                    | 7.12 ms: 1.01x faster                                                         |
| json                     | 5.31 ms                                                    | 5.24 ms: 1.01x faster                                                         |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 5.21 ms: 1.01x faster                                                         |
| pprint_pformat           | 1.56 sec                                                   | 1.54 sec: 1.01x faster                                                        |
| json_dumps               | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                         |
| pidigits                 | 191 ms                                                     | 190 ms: 1.01x faster                                                          |
| 2to3                     | 274 ms                                                     | 272 ms: 1.01x faster                                                          |
| pprint_safe_repr         | 758 ms                                                     | 752 ms: 1.01x faster                                                          |
| deltablue                | 3.25 ms                                                    | 3.23 ms: 1.01x faster                                                         |
| dulwich_log              | 67.2 ms                                                    | 66.7 ms: 1.01x faster                                                         |
| aiohttp                  | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                         |
| raytrace                 | 267 ms                                                     | 265 ms: 1.01x faster                                                          |
| xml_etree_process        | 61.2 ms                                                    | 60.8 ms: 1.01x faster                                                         |
| generators               | 29.6 ms                                                    | 29.5 ms: 1.01x faster                                                         |
| python_startup_no_site   | 7.11 ms                                                    | 7.07 ms: 1.01x faster                                                         |
| nqueens                  | 81.4 ms                                                    | 81.0 ms: 1.00x faster                                                         |
| scimark_monte_carlo      | 69.2 ms                                                    | 68.9 ms: 1.00x faster                                                         |
| regex_compile            | 137 ms                                                     | 136 ms: 1.00x faster                                                          |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.85 sec: 1.00x slower                                                        |
| docutils                 | 2.83 sec                                                   | 2.84 sec: 1.00x slower                                                        |
| asyncio_websockets       | 567 ms                                                     | 569 ms: 1.00x slower                                                          |
| mdp                      | 2.79 sec                                                   | 2.80 sec: 1.01x slower                                                        |
| sqlglot_normalize        | 110 ms                                                     | 111 ms: 1.01x slower                                                          |
| sympy_expand             | 473 ms                                                     | 476 ms: 1.01x slower                                                          |
| meteor_contest           | 110 ms                                                     | 111 ms: 1.01x slower                                                          |
| bench_thread_pool        | 834 us                                                     | 840 us: 1.01x slower                                                          |
| django_template          | 34.8 ms                                                    | 35.1 ms: 1.01x slower                                                         |
| genshi_xml               | 51.6 ms                                                    | 52.1 ms: 1.01x slower                                                         |
| async_generators         | 442 ms                                                     | 446 ms: 1.01x slower                                                          |
| regex_v8                 | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                         |
| xml_etree_generate       | 87.4 ms                                                    | 88.3 ms: 1.01x slower                                                         |
| sympy_sum                | 156 ms                                                     | 157 ms: 1.01x slower                                                          |
| logging_simple           | 5.74 us                                                    | 5.81 us: 1.01x slower                                                         |
| pycparser                | 1.16 sec                                                   | 1.17 sec: 1.01x slower                                                        |
| regex_dna                | 221 ms                                                     | 224 ms: 1.01x slower                                                          |
| hexiom                   | 6.30 ms                                                    | 6.38 ms: 1.01x slower                                                         |
| regex_effbot             | 3.67 ms                                                    | 3.73 ms: 1.01x slower                                                         |
| unpickle_pure_python     | 218 us                                                     | 222 us: 1.02x slower                                                          |
| html5lib                 | 67.2 ms                                                    | 68.6 ms: 1.02x slower                                                         |
| telco                    | 8.41 ms                                                    | 8.60 ms: 1.02x slower                                                         |
| comprehensions           | 16.6 us                                                    | 17.0 us: 1.03x slower                                                         |
| unpickle                 | 15.1 us                                                    | 15.5 us: 1.03x slower                                                         |
| pickle_dict              | 34.8 us                                                    | 36.0 us: 1.03x slower                                                         |
| coverage                 | 93.1 ms                                                    | 97.7 ms: 1.05x slower                                                         |
| spectral_norm            | 116 ms                                                     | 122 ms: 1.05x slower                                                          |
| pickle                   | 11.5 us                                                    | 12.1 us: 1.05x slower                                                         |
| tomli_loads              | 2.12 sec                                                   | 2.24 sec: 1.06x slower                                                        |
| pickle_list              | 5.11 us                                                    | 5.41 us: 1.06x slower                                                         |
| Geometric mean           | (ref)                                                      | 1.01x faster                                                                  |

Benchmark hidden because not significant (26): async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization, gunicorn, bench_mp_pool, go, async_tree_none_tg, xml_etree_iterparse, mypy2, fannkuch, pyflate, pickle_pure_python, sqlglot_optimize, asyncio_tcp, async_tree_memoization_tg, tornado_http, logging_format, sympy_integrate, genshi_text, sympy_str, pathlib, dask, logging_silent, djangocms, pylint, async_tree_cpu_io_mixed_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 94.45% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x