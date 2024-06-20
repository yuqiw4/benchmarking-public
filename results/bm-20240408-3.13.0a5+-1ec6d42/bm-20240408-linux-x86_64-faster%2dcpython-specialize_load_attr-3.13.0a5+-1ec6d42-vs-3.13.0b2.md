# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 1ec6d42
- commit date: 2024-04-08
- overall geometric mean: 1.01x faster
- HPT reliability: 65.72%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 271 ms: 1.01x faster                                                             |
| chameleon      | 7.22 ms                                                    | 7.01 ms: 1.03x faster                                                            |
| html5lib       | 67.2 ms                                                    | 68.9 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 352 ms: 1.08x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 609 ms: 1.04x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_io_tg, async_tree_none_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| float          | 78.9 ms                                                    | 79.3 ms: 1.01x slower                                                            |
| nbody          | 88.3 ms                                                    | 89.5 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 136 ms: 1.01x faster                                                             |
| regex_v8       | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                            |
| regex_dna      | 221 ms                                                     | 232 ms: 1.05x slower                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.86 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                      | 1.03x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.00 us: 1.07x faster                                                            |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| xml_etree_process    | 61.2 ms                                                    | 60.5 ms: 1.01x faster                                                            |
| json_loads           | 28.9 us                                                    | 28.7 us: 1.01x faster                                                            |
| unpickle             | 15.1 us                                                    | 15.2 us: 1.01x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 87.9 ms: 1.01x slower                                                            |
| pickle_dict          | 34.8 us                                                    | 35.4 us: 1.02x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.16 sec: 1.02x slower                                                           |
| unpickle_pure_python | 218 us                                                     | 226 us: 1.04x slower                                                             |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                                            |
| pickle_list          | 5.11 us                                                    | 5.35 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 8.93 ms: 1.26x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                            |
| genshi_text    | 23.7 ms                                                    | 23.8 ms: 1.01x slower                                                            |
| genshi_xml     | 51.6 ms                                                    | 52.6 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 114 us: 1.44x faster                                                             |
| pylint                     | 317 ms                                                     | 282 ms: 1.13x faster                                                             |
| scimark_fft                | 392 ms                                                     | 362 ms: 1.08x faster                                                             |
| async_tree_none            | 378 ms                                                     | 352 ms: 1.08x faster                                                             |
| richards                   | 50.9 ms                                                    | 47.4 ms: 1.07x faster                                                            |
| unpickle_list              | 5.34 us                                                    | 5.00 us: 1.07x faster                                                            |
| richards_super             | 57.4 ms                                                    | 53.7 ms: 1.07x faster                                                            |
| scimark_lu                 | 122 ms                                                     | 114 ms: 1.06x faster                                                             |
| gc_traversal               | 3.98 ms                                                    | 3.76 ms: 1.06x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.73 ms: 1.05x faster                                                            |
| coroutines                 | 23.2 ms                                                    | 22.1 ms: 1.05x faster                                                            |
| mdp                        | 2.79 sec                                                   | 2.65 sec: 1.05x faster                                                           |
| deepcopy_memo              | 39.7 us                                                    | 38.2 us: 1.04x faster                                                            |
| spectral_norm              | 116 ms                                                     | 112 ms: 1.04x faster                                                             |
| pyflate                    | 484 ms                                                     | 469 ms: 1.03x faster                                                             |
| chameleon                  | 7.22 ms                                                    | 7.01 ms: 1.03x faster                                                            |
| logging_silent             | 105 ns                                                     | 102 ns: 1.03x faster                                                             |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                            |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.15 ms: 1.02x faster                                                            |
| fannkuch                   | 402 ms                                                     | 393 ms: 1.02x faster                                                             |
| scimark_sor                | 127 ms                                                     | 125 ms: 1.02x faster                                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                            |
| mako                       | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 76.0 ms: 1.02x faster                                                            |
| sqlite_synth               | 2.99 us                                                    | 2.93 us: 1.02x faster                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.30 ms: 1.02x faster                                                            |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.1 ms: 1.02x faster                                                            |
| thrift                     | 823 us                                                     | 811 us: 1.01x faster                                                             |
| xml_etree_process          | 61.2 ms                                                    | 60.5 ms: 1.01x faster                                                            |
| 2to3                       | 274 ms                                                     | 271 ms: 1.01x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                    | 3.32 us: 1.01x faster                                                            |
| chaos                      | 61.3 ms                                                    | 60.8 ms: 1.01x faster                                                            |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| deepcopy                   | 367 us                                                     | 364 us: 1.01x faster                                                             |
| regex_compile              | 137 ms                                                     | 136 ms: 1.01x faster                                                             |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                            |
| json_loads                 | 28.9 us                                                    | 28.7 us: 1.01x faster                                                            |
| raytrace                   | 267 ms                                                     | 265 ms: 1.00x faster                                                             |
| go                         | 145 ms                                                     | 144 ms: 1.00x faster                                                             |
| sympy_integrate            | 20.5 ms                                                    | 20.6 ms: 1.00x slower                                                            |
| unpickle                   | 15.1 us                                                    | 15.2 us: 1.01x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 87.9 ms: 1.01x slower                                                            |
| float                      | 78.9 ms                                                    | 79.3 ms: 1.01x slower                                                            |
| bench_thread_pool          | 834 us                                                     | 839 us: 1.01x slower                                                             |
| dulwich_log                | 67.2 ms                                                    | 67.6 ms: 1.01x slower                                                            |
| deltablue                  | 3.25 ms                                                    | 3.27 ms: 1.01x slower                                                            |
| genshi_text                | 23.7 ms                                                    | 23.8 ms: 1.01x slower                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 55.9 ms: 1.01x slower                                                            |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                             |
| asyncio_tcp                | 508 ms                                                     | 513 ms: 1.01x slower                                                             |
| sympy_sum                  | 156 ms                                                     | 157 ms: 1.01x slower                                                             |
| regex_v8                   | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                            |
| generators                 | 29.6 ms                                                    | 30.0 ms: 1.01x slower                                                            |
| comprehensions             | 16.6 us                                                    | 16.8 us: 1.01x slower                                                            |
| logging_format             | 6.47 us                                                    | 6.55 us: 1.01x slower                                                            |
| nbody                      | 88.3 ms                                                    | 89.5 ms: 1.01x slower                                                            |
| async_generators           | 442 ms                                                     | 448 ms: 1.01x slower                                                             |
| json                       | 5.31 ms                                                    | 5.38 ms: 1.01x slower                                                            |
| telco                      | 8.41 ms                                                    | 8.54 ms: 1.02x slower                                                            |
| pickle_dict                | 34.8 us                                                    | 35.4 us: 1.02x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.16 sec: 1.02x slower                                                           |
| genshi_xml                 | 51.6 ms                                                    | 52.6 ms: 1.02x slower                                                            |
| sqlglot_normalize          | 110 ms                                                     | 112 ms: 1.02x slower                                                             |
| logging_simple             | 5.74 us                                                    | 5.88 us: 1.02x slower                                                            |
| html5lib                   | 67.2 ms                                                    | 68.9 ms: 1.02x slower                                                            |
| nqueens                    | 81.4 ms                                                    | 83.7 ms: 1.03x slower                                                            |
| hexiom                     | 6.30 ms                                                    | 6.47 ms: 1.03x slower                                                            |
| unpickle_pure_python       | 218 us                                                     | 226 us: 1.04x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 609 ms: 1.04x slower                                                             |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.04x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.21 sec: 1.04x slower                                                           |
| coverage                   | 93.1 ms                                                    | 97.2 ms: 1.04x slower                                                            |
| pickle_list                | 5.11 us                                                    | 5.35 us: 1.05x slower                                                            |
| regex_dna                  | 221 ms                                                     | 232 ms: 1.05x slower                                                             |
| regex_effbot               | 3.67 ms                                                    | 3.86 ms: 1.05x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 18.8 ms: 1.09x slower                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 8.93 ms: 1.26x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (21): async_tree_io, async_tree_io_tg, xml_etree_parse, async_tree_none_tg, async_tree_memoization, gunicorn, dask, sympy_str, async_tree_memoization_tg, tornado_http, xml_etree_iterparse, pickle_pure_python, sympy_expand, asyncio_websockets, asyncio_tcp_ssl, mypy2, bench_mp_pool, docutils, pprint_pformat, pprint_safe_repr, async_tree_cpu_io_mixed
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 65.72% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x