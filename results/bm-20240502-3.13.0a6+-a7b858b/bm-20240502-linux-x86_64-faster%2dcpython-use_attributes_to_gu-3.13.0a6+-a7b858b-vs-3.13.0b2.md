# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: a7b858b
- commit date: 2024-05-02
- overall geometric mean: 1.01x faster
- HPT reliability: 98.24%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 272 ms: 1.01x faster                                                             |
| docutils       | 2.83 sec                                                   | 2.82 sec: 1.00x faster                                                           |
| html5lib       | 67.2 ms                                                    | 70.3 ms: 1.05x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 93.2 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 352 ms: 1.07x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 614 ms: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 193 ms: 1.01x slower                                                             |
| nbody          | 88.3 ms                                                    | 89.5 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.6 ms: 1.02x faster                                                            |
| regex_effbot   | 3.67 ms                                                    | 3.62 ms: 1.01x faster                                                            |
| regex_compile  | 137 ms                                                     | 135 ms: 1.01x faster                                                             |
| regex_dna      | 221 ms                                                     | 224 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.19 us: 1.03x faster                                                            |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| json_loads           | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| xml_etree_iterparse  | 107 ms                                                     | 107 ms: 1.01x faster                                                             |
| xml_etree_generate   | 87.4 ms                                                    | 88.0 ms: 1.01x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.13 sec: 1.01x slower                                                           |
| unpickle_pure_python | 218 us                                                     | 220 us: 1.01x slower                                                             |
| pickle_list          | 5.11 us                                                    | 5.16 us: 1.01x slower                                                            |
| unpickle             | 15.1 us                                                    | 15.5 us: 1.02x slower                                                            |
| pickle_dict          | 34.8 us                                                    | 35.9 us: 1.03x slower                                                            |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                                            |
| pickle_pure_python   | 305 us                                                     | 320 us: 1.05x slower                                                             |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                                     |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text    | 23.7 ms                                                    | 23.0 ms: 1.03x faster                                                            |
| genshi_xml     | 51.6 ms                                                    | 50.8 ms: 1.02x faster                                                            |
| mako           | 11.2 ms                                                    | 11.3 ms: 1.00x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| go                         | 145 ms                                                     | 119 ms: 1.21x faster                                                             |
| async_tree_none            | 378 ms                                                     | 352 ms: 1.07x faster                                                             |
| richards                   | 50.9 ms                                                    | 47.4 ms: 1.07x faster                                                            |
| richards_super             | 57.4 ms                                                    | 53.5 ms: 1.07x faster                                                            |
| scimark_fft                | 392 ms                                                     | 368 ms: 1.07x faster                                                             |
| deepcopy_memo              | 39.7 us                                                    | 37.6 us: 1.06x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.18 us: 1.05x faster                                                            |
| scimark_lu                 | 122 ms                                                     | 116 ms: 1.05x faster                                                             |
| gc_traversal               | 3.98 ms                                                    | 3.81 ms: 1.04x faster                                                            |
| coroutines                 | 23.2 ms                                                    | 22.2 ms: 1.04x faster                                                            |
| logging_silent             | 105 ns                                                     | 101 ns: 1.04x faster                                                             |
| spectral_norm              | 116 ms                                                     | 112 ms: 1.03x faster                                                             |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                            |
| sqlite_synth               | 2.99 us                                                    | 2.90 us: 1.03x faster                                                            |
| unpickle_list              | 5.34 us                                                    | 5.19 us: 1.03x faster                                                            |
| genshi_text                | 23.7 ms                                                    | 23.0 ms: 1.03x faster                                                            |
| pyflate                    | 484 ms                                                     | 470 ms: 1.03x faster                                                             |
| deepcopy                   | 367 us                                                     | 358 us: 1.03x faster                                                             |
| dulwich_log                | 67.2 ms                                                    | 65.5 ms: 1.03x faster                                                            |
| nqueens                    | 81.4 ms                                                    | 79.6 ms: 1.02x faster                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| logging_format             | 6.47 us                                                    | 6.33 us: 1.02x faster                                                            |
| regex_v8                   | 25.1 ms                                                    | 24.6 ms: 1.02x faster                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                            |
| fannkuch                   | 402 ms                                                     | 394 ms: 1.02x faster                                                             |
| raytrace                   | 267 ms                                                     | 262 ms: 1.02x faster                                                             |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| tornado_http               | 94.6 ms                                                    | 93.2 ms: 1.02x faster                                                            |
| genshi_xml                 | 51.6 ms                                                    | 50.8 ms: 1.02x faster                                                            |
| chaos                      | 61.3 ms                                                    | 60.5 ms: 1.01x faster                                                            |
| meteor_contest             | 110 ms                                                     | 108 ms: 1.01x faster                                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.20 ms: 1.01x faster                                                            |
| json_loads                 | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.62 ms: 1.01x faster                                                            |
| regex_compile              | 137 ms                                                     | 135 ms: 1.01x faster                                                             |
| hexiom                     | 6.30 ms                                                    | 6.22 ms: 1.01x faster                                                            |
| gunicorn                   | 1.28 ms                                                    | 1.26 ms: 1.01x faster                                                            |
| sympy_integrate            | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                                            |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                            |
| generators                 | 29.6 ms                                                    | 29.4 ms: 1.01x faster                                                            |
| 2to3                       | 274 ms                                                     | 272 ms: 1.01x faster                                                             |
| xml_etree_iterparse        | 107 ms                                                     | 107 ms: 1.01x faster                                                             |
| sympy_sum                  | 156 ms                                                     | 155 ms: 1.01x faster                                                             |
| bench_thread_pool          | 834 us                                                     | 828 us: 1.01x faster                                                             |
| logging_simple             | 5.74 us                                                    | 5.70 us: 1.01x faster                                                            |
| deltablue                  | 3.25 ms                                                    | 3.23 ms: 1.01x faster                                                            |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                             |
| asyncio_tcp                | 508 ms                                                     | 506 ms: 1.00x faster                                                             |
| docutils                   | 2.83 sec                                                   | 2.82 sec: 1.00x faster                                                           |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x faster                                                           |
| pprint_safe_repr           | 758 ms                                                     | 761 ms: 1.00x slower                                                             |
| mako                       | 11.2 ms                                                    | 11.3 ms: 1.00x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 88.0 ms: 1.01x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.13 sec: 1.01x slower                                                           |
| coverage                   | 93.1 ms                                                    | 93.8 ms: 1.01x slower                                                            |
| pidigits                   | 191 ms                                                     | 193 ms: 1.01x slower                                                             |
| unpickle_pure_python       | 218 us                                                     | 220 us: 1.01x slower                                                             |
| pickle_list                | 5.11 us                                                    | 5.16 us: 1.01x slower                                                            |
| telco                      | 8.41 ms                                                    | 8.50 ms: 1.01x slower                                                            |
| nbody                      | 88.3 ms                                                    | 89.5 ms: 1.01x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 17.6 ms: 1.01x slower                                                            |
| regex_dna                  | 221 ms                                                     | 224 ms: 1.01x slower                                                             |
| unpickle                   | 15.1 us                                                    | 15.5 us: 1.02x slower                                                            |
| pickle_dict                | 34.8 us                                                    | 35.9 us: 1.03x slower                                                            |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.04x slower                                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 614 ms: 1.05x slower                                                             |
| html5lib                   | 67.2 ms                                                    | 70.3 ms: 1.05x slower                                                            |
| scimark_sor                | 127 ms                                                     | 134 ms: 1.05x slower                                                             |
| pickle_pure_python         | 305 us                                                     | 320 us: 1.05x slower                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 74.2 ms: 1.07x slower                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 83.7 ms: 1.08x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (29): xml_etree_parse, async_tree_io, djangocms, sympy_str, dask, pycparser, mypy2, async_tree_memoization, xml_etree_process, pprint_pformat, django_template, sqlglot_optimize, bench_mp_pool, async_generators, thrift, chameleon, float, typing_runtime_protocols, python_startup_no_site, mdp, sqlglot_normalize, sympy_expand, pylint, async_tree_cpu_io_mixed, comprehensions, json, async_tree_none_tg, async_tree_memoization_tg, async_tree_io_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 98.24% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x