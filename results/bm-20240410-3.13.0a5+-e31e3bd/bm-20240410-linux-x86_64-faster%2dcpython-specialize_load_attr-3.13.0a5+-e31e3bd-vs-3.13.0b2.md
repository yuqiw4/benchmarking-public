# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: e31e3bd
- commit date: 2024-04-10
- overall geometric mean: 1.01x faster
- HPT reliability: 80.28%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 273 ms: 1.01x faster                                                             |
| chameleon      | 7.22 ms                                                    | 7.05 ms: 1.02x faster                                                            |
| html5lib       | 67.2 ms                                                    | 67.8 ms: 1.01x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 93.9 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 352 ms: 1.08x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 221 ms                                                     | 225 ms: 1.02x slower                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.75 ms: 1.02x slower                                                            |
| regex_v8       | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                      | 1.02x slower                                                                     |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_dict          | 34.8 us                                                    | 32.1 us: 1.08x faster                                                            |
| pickle_list          | 5.11 us                                                    | 4.92 us: 1.04x faster                                                            |
| xml_etree_parse      | 162 ms                                                     | 159 ms: 1.02x faster                                                             |
| unpickle_list        | 5.34 us                                                    | 5.27 us: 1.01x faster                                                            |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| xml_etree_process    | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                                            |
| pickle_pure_python   | 305 us                                                     | 304 us: 1.01x faster                                                             |
| xml_etree_generate   | 87.4 ms                                                    | 88.0 ms: 1.01x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                           |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                                            |
| unpickle_pure_python | 218 us                                                     | 228 us: 1.04x slower                                                             |
| unpickle             | 15.1 us                                                    | 15.9 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 8.93 ms: 1.26x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 11.1 ms: 1.01x faster                                                            |
| genshi_text    | 23.7 ms                                                    | 24.6 ms: 1.04x slower                                                            |
| genshi_xml     | 51.6 ms                                                    | 53.6 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                      | 1.02x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 117 us: 1.41x faster                                                             |
| pylint                     | 317 ms                                                     | 280 ms: 1.13x faster                                                             |
| pickle_dict                | 34.8 us                                                    | 32.1 us: 1.08x faster                                                            |
| async_tree_none            | 378 ms                                                     | 352 ms: 1.08x faster                                                             |
| richards_super             | 57.4 ms                                                    | 54.0 ms: 1.06x faster                                                            |
| richards                   | 50.9 ms                                                    | 48.0 ms: 1.06x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.75 ms: 1.06x faster                                                            |
| scimark_fft                | 392 ms                                                     | 372 ms: 1.06x faster                                                             |
| create_gc_cycles           | 1.82 ms                                                    | 1.72 ms: 1.06x faster                                                            |
| mdp                        | 2.79 sec                                                   | 2.66 sec: 1.05x faster                                                           |
| crypto_pyaes               | 77.5 ms                                                    | 74.0 ms: 1.05x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.22 us: 1.04x faster                                                            |
| spectral_norm              | 116 ms                                                     | 112 ms: 1.04x faster                                                             |
| pickle_list                | 5.11 us                                                    | 4.92 us: 1.04x faster                                                            |
| coroutines                 | 23.2 ms                                                    | 22.4 ms: 1.04x faster                                                            |
| thrift                     | 823 us                                                     | 801 us: 1.03x faster                                                             |
| deepcopy                   | 367 us                                                     | 358 us: 1.03x faster                                                             |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                            |
| fannkuch                   | 402 ms                                                     | 392 ms: 1.03x faster                                                             |
| scimark_sor                | 127 ms                                                     | 124 ms: 1.03x faster                                                             |
| scimark_lu                 | 122 ms                                                     | 119 ms: 1.03x faster                                                             |
| chameleon                  | 7.22 ms                                                    | 7.05 ms: 1.02x faster                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                            |
| scimark_monte_carlo        | 69.2 ms                                                    | 67.8 ms: 1.02x faster                                                            |
| deepcopy_memo              | 39.7 us                                                    | 38.9 us: 1.02x faster                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.30 ms: 1.02x faster                                                            |
| raytrace                   | 267 ms                                                     | 262 ms: 1.02x faster                                                             |
| xml_etree_parse            | 162 ms                                                     | 159 ms: 1.02x faster                                                             |
| unpickle_list              | 5.34 us                                                    | 5.27 us: 1.01x faster                                                            |
| chaos                      | 61.3 ms                                                    | 60.5 ms: 1.01x faster                                                            |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| mako                       | 11.2 ms                                                    | 11.1 ms: 1.01x faster                                                            |
| sqlite_synth               | 2.99 us                                                    | 2.96 us: 1.01x faster                                                            |
| xml_etree_process          | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                                            |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| tornado_http               | 94.6 ms                                                    | 93.9 ms: 1.01x faster                                                            |
| pyflate                    | 484 ms                                                     | 481 ms: 1.01x faster                                                             |
| pprint_pformat             | 1.56 sec                                                   | 1.54 sec: 1.01x faster                                                           |
| go                         | 145 ms                                                     | 144 ms: 1.01x faster                                                             |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                            |
| pickle_pure_python         | 305 us                                                     | 304 us: 1.01x faster                                                             |
| 2to3                       | 274 ms                                                     | 273 ms: 1.01x faster                                                             |
| logging_silent             | 105 ns                                                     | 105 ns: 1.00x slower                                                             |
| sympy_expand               | 473 ms                                                     | 474 ms: 1.00x slower                                                             |
| bench_thread_pool          | 834 us                                                     | 837 us: 1.00x slower                                                             |
| async_generators           | 442 ms                                                     | 444 ms: 1.00x slower                                                             |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.85 sec: 1.00x slower                                                           |
| asyncio_websockets         | 567 ms                                                     | 570 ms: 1.00x slower                                                             |
| sympy_sum                  | 156 ms                                                     | 157 ms: 1.01x slower                                                             |
| xml_etree_generate         | 87.4 ms                                                    | 88.0 ms: 1.01x slower                                                            |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                             |
| html5lib                   | 67.2 ms                                                    | 67.8 ms: 1.01x slower                                                            |
| deltablue                  | 3.25 ms                                                    | 3.29 ms: 1.01x slower                                                            |
| nqueens                    | 81.4 ms                                                    | 82.7 ms: 1.02x slower                                                            |
| sqlglot_normalize          | 110 ms                                                     | 112 ms: 1.02x slower                                                             |
| regex_dna                  | 221 ms                                                     | 225 ms: 1.02x slower                                                             |
| comprehensions             | 16.6 us                                                    | 16.9 us: 1.02x slower                                                            |
| logging_simple             | 5.74 us                                                    | 5.86 us: 1.02x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                           |
| regex_effbot               | 3.67 ms                                                    | 3.75 ms: 1.02x slower                                                            |
| telco                      | 8.41 ms                                                    | 8.62 ms: 1.02x slower                                                            |
| regex_v8                   | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                                            |
| hexiom                     | 6.30 ms                                                    | 6.48 ms: 1.03x slower                                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                             |
| generators                 | 29.6 ms                                                    | 30.7 ms: 1.04x slower                                                            |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.04x slower                                                            |
| genshi_text                | 23.7 ms                                                    | 24.6 ms: 1.04x slower                                                            |
| genshi_xml                 | 51.6 ms                                                    | 53.6 ms: 1.04x slower                                                            |
| unpickle_pure_python       | 218 us                                                     | 228 us: 1.04x slower                                                             |
| coverage                   | 93.1 ms                                                    | 97.3 ms: 1.05x slower                                                            |
| unpickle                   | 15.1 us                                                    | 15.9 us: 1.05x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 18.8 ms: 1.09x slower                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 8.93 ms: 1.26x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (26): async_tree_io, async_tree_memoization_tg, scimark_sparse_mat_mult, async_tree_none_tg, json_loads, gunicorn, dask, float, pprint_safe_repr, mypy2, sympy_str, asyncio_tcp, regex_compile, nbody, async_tree_memoization, sqlglot_optimize, dulwich_log, async_tree_io_tg, sympy_integrate, async_tree_cpu_io_mixed, docutils, bench_mp_pool, logging_format, xml_etree_iterparse, json, pycparser
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 80.28% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x