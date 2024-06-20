# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: 83ebcf5
- commit date: 2024-04-16
- overall geometric mean: 1.01x faster
- HPT reliability: 56.92%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 271 ms: 1.01x faster                                                          |
| chameleon      | 7.22 ms                                                    | 7.07 ms: 1.02x faster                                                         |
| html5lib       | 67.2 ms                                                    | 68.2 ms: 1.01x slower                                                         |
| tornado_http   | 94.6 ms                                                    | 94.1 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                  |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 357 ms: 1.06x faster                                                          |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 604 ms: 1.03x slower                                                          |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                                  |

Benchmark hidden because not significant (6): async_tree_io, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                          |
| float          | 78.9 ms                                                    | 79.8 ms: 1.01x slower                                                         |
| nbody          | 88.3 ms                                                    | 90.3 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.8 ms: 1.01x faster                                                         |
| regex_effbot   | 3.67 ms                                                    | 3.65 ms: 1.01x faster                                                         |
| regex_compile  | 137 ms                                                     | 137 ms: 1.00x slower                                                          |
| regex_dna      | 221 ms                                                     | 226 ms: 1.02x slower                                                          |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 4.98 us: 1.07x faster                                                         |
| json_loads           | 28.9 us                                                    | 28.0 us: 1.03x faster                                                         |
| pickle_dict          | 34.8 us                                                    | 33.9 us: 1.03x faster                                                         |
| pickle_list          | 5.11 us                                                    | 5.03 us: 1.01x faster                                                         |
| xml_etree_parse      | 162 ms                                                     | 160 ms: 1.01x faster                                                          |
| pickle_pure_python   | 305 us                                                     | 302 us: 1.01x faster                                                          |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                         |
| xml_etree_generate   | 87.4 ms                                                    | 88.5 ms: 1.01x slower                                                         |
| unpickle_pure_python | 218 us                                                     | 223 us: 1.02x slower                                                          |
| tomli_loads          | 2.12 sec                                                   | 2.22 sec: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                                  |

Benchmark hidden because not significant (4): xml_etree_process, unpickle, pickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                         |
| python_startup_no_site | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                                         |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 11.0 ms: 1.03x faster                                                         |
| genshi_text     | 23.7 ms                                                    | 23.8 ms: 1.00x slower                                                         |
| django_template | 34.8 ms                                                    | 35.6 ms: 1.02x slower                                                         |
| Geometric mean  | (ref)                                                      | 1.00x slower                                                                  |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 113 us: 1.46x faster                                                          |
| unpickle_list              | 5.34 us                                                    | 4.98 us: 1.07x faster                                                         |
| richards_super             | 57.4 ms                                                    | 54.0 ms: 1.06x faster                                                         |
| async_tree_none            | 378 ms                                                     | 357 ms: 1.06x faster                                                          |
| gc_traversal               | 3.98 ms                                                    | 3.76 ms: 1.06x faster                                                         |
| richards                   | 50.9 ms                                                    | 48.2 ms: 1.06x faster                                                         |
| create_gc_cycles           | 1.82 ms                                                    | 1.73 ms: 1.05x faster                                                         |
| mdp                        | 2.79 sec                                                   | 2.67 sec: 1.04x faster                                                        |
| scimark_fft                | 392 ms                                                     | 380 ms: 1.03x faster                                                          |
| deepcopy_memo              | 39.7 us                                                    | 38.5 us: 1.03x faster                                                         |
| pyflate                    | 484 ms                                                     | 469 ms: 1.03x faster                                                          |
| json_loads                 | 28.9 us                                                    | 28.0 us: 1.03x faster                                                         |
| deepcopy_reduce            | 3.35 us                                                    | 3.26 us: 1.03x faster                                                         |
| pickle_dict                | 34.8 us                                                    | 33.9 us: 1.03x faster                                                         |
| mako                       | 11.2 ms                                                    | 11.0 ms: 1.03x faster                                                         |
| crypto_pyaes               | 77.5 ms                                                    | 75.6 ms: 1.02x faster                                                         |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                         |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                         |
| scimark_sor                | 127 ms                                                     | 125 ms: 1.02x faster                                                          |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                         |
| chameleon                  | 7.22 ms                                                    | 7.07 ms: 1.02x faster                                                         |
| json                       | 5.31 ms                                                    | 5.21 ms: 1.02x faster                                                         |
| deepcopy                   | 367 us                                                     | 361 us: 1.02x faster                                                          |
| pickle_list                | 5.11 us                                                    | 5.03 us: 1.01x faster                                                         |
| thrift                     | 823 us                                                     | 811 us: 1.01x faster                                                          |
| regex_v8                   | 25.1 ms                                                    | 24.8 ms: 1.01x faster                                                         |
| xml_etree_parse            | 162 ms                                                     | 160 ms: 1.01x faster                                                          |
| dulwich_log                | 67.2 ms                                                    | 66.3 ms: 1.01x faster                                                         |
| pickle_pure_python         | 305 us                                                     | 302 us: 1.01x faster                                                          |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                         |
| 2to3                       | 274 ms                                                     | 271 ms: 1.01x faster                                                          |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                          |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                         |
| pprint_pformat             | 1.56 sec                                                   | 1.54 sec: 1.01x faster                                                        |
| fannkuch                   | 402 ms                                                     | 399 ms: 1.01x faster                                                          |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                          |
| logging_format             | 6.47 us                                                    | 6.43 us: 1.01x faster                                                         |
| raytrace                   | 267 ms                                                     | 265 ms: 1.01x faster                                                          |
| spectral_norm              | 116 ms                                                     | 115 ms: 1.01x faster                                                          |
| asyncio_tcp                | 508 ms                                                     | 505 ms: 1.01x faster                                                          |
| regex_effbot               | 3.67 ms                                                    | 3.65 ms: 1.01x faster                                                         |
| tornado_http               | 94.6 ms                                                    | 94.1 ms: 1.01x faster                                                         |
| logging_silent             | 105 ns                                                     | 104 ns: 1.01x faster                                                          |
| pprint_safe_repr           | 758 ms                                                     | 755 ms: 1.00x faster                                                          |
| python_startup_no_site     | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                                         |
| regex_compile              | 137 ms                                                     | 137 ms: 1.00x slower                                                          |
| sympy_integrate            | 20.5 ms                                                    | 20.6 ms: 1.00x slower                                                         |
| genshi_text                | 23.7 ms                                                    | 23.8 ms: 1.00x slower                                                         |
| bench_thread_pool          | 834 us                                                     | 838 us: 1.01x slower                                                          |
| logging_simple             | 5.74 us                                                    | 5.78 us: 1.01x slower                                                         |
| sqlglot_optimize           | 55.5 ms                                                    | 56.0 ms: 1.01x slower                                                         |
| float                      | 78.9 ms                                                    | 79.8 ms: 1.01x slower                                                         |
| nqueens                    | 81.4 ms                                                    | 82.4 ms: 1.01x slower                                                         |
| xml_etree_generate         | 87.4 ms                                                    | 88.5 ms: 1.01x slower                                                         |
| async_generators           | 442 ms                                                     | 448 ms: 1.01x slower                                                          |
| sympy_sum                  | 156 ms                                                     | 158 ms: 1.01x slower                                                          |
| sympy_expand               | 473 ms                                                     | 479 ms: 1.01x slower                                                          |
| deltablue                  | 3.25 ms                                                    | 3.29 ms: 1.01x slower                                                         |
| chaos                      | 61.3 ms                                                    | 62.2 ms: 1.01x slower                                                         |
| pathlib                    | 17.3 ms                                                    | 17.6 ms: 1.01x slower                                                         |
| generators                 | 29.6 ms                                                    | 30.1 ms: 1.01x slower                                                         |
| html5lib                   | 67.2 ms                                                    | 68.2 ms: 1.01x slower                                                         |
| pycparser                  | 1.16 sec                                                   | 1.18 sec: 1.01x slower                                                        |
| sqlglot_normalize          | 110 ms                                                     | 112 ms: 1.02x slower                                                          |
| meteor_contest             | 110 ms                                                     | 112 ms: 1.02x slower                                                          |
| hexiom                     | 6.30 ms                                                    | 6.40 ms: 1.02x slower                                                         |
| scimark_monte_carlo        | 69.2 ms                                                    | 70.3 ms: 1.02x slower                                                         |
| regex_dna                  | 221 ms                                                     | 226 ms: 1.02x slower                                                          |
| unpickle_pure_python       | 218 us                                                     | 223 us: 1.02x slower                                                          |
| django_template            | 34.8 ms                                                    | 35.6 ms: 1.02x slower                                                         |
| nbody                      | 88.3 ms                                                    | 90.3 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 604 ms: 1.03x slower                                                          |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.46 ms: 1.04x slower                                                         |
| comprehensions             | 16.6 us                                                    | 17.2 us: 1.04x slower                                                         |
| coverage                   | 93.1 ms                                                    | 97.6 ms: 1.05x slower                                                         |
| tomli_loads                | 2.12 sec                                                   | 2.22 sec: 1.05x slower                                                        |
| telco                      | 8.41 ms                                                    | 8.85 ms: 1.05x slower                                                         |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                  |

Benchmark hidden because not significant (24): async_tree_io, async_tree_cpu_io_mixed, sqlite_synth, gunicorn, scimark_lu, dask, go, bench_mp_pool, mypy2, coroutines, asyncio_tcp_ssl, xml_etree_process, unpickle, async_tree_io_tg, async_tree_memoization_tg, pickle, xml_etree_iterparse, docutils, async_tree_none_tg, genshi_xml, async_tree_memoization, sympy_str, djangocms, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 56.92% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x