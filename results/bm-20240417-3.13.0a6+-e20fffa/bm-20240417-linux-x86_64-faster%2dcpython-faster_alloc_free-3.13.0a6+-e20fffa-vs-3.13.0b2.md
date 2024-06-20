# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: e20fffa
- commit date: 2024-04-17
- overall geometric mean: 1.01x faster
- HPT reliability: 96.77%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 271 ms: 1.01x faster                                                          |
| docutils       | 2.83 sec                                                   | 2.84 sec: 1.00x slower                                                        |
| tornado_http   | 94.6 ms                                                    | 94.1 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                  |

Benchmark hidden because not significant (2): chameleon, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 358 ms: 1.06x faster                                                          |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 607 ms: 1.03x slower                                                          |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                                  |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 85.0 ms: 1.04x faster                                                         |
| float          | 78.9 ms                                                    | 77.2 ms: 1.02x faster                                                         |
| pidigits       | 191 ms                                                     | 191 ms: 1.00x faster                                                          |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 135 ms: 1.01x faster                                                          |
| regex_v8       | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                         |
| regex_effbot   | 3.67 ms                                                    | 3.74 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                  |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|---------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_dict         | 34.8 us                                                    | 32.7 us: 1.06x faster                                                         |
| unpickle_list       | 5.34 us                                                    | 5.08 us: 1.05x faster                                                         |
| json_loads          | 28.9 us                                                    | 27.5 us: 1.05x faster                                                         |
| pickle_list         | 5.11 us                                                    | 4.89 us: 1.04x faster                                                         |
| pickle_pure_python  | 305 us                                                     | 299 us: 1.02x faster                                                          |
| unpickle            | 15.1 us                                                    | 14.8 us: 1.02x faster                                                         |
| json_dumps          | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                         |
| xml_etree_iterparse | 107 ms                                                     | 108 ms: 1.01x slower                                                          |
| pickle              | 11.5 us                                                    | 11.6 us: 1.01x slower                                                         |
| xml_etree_generate  | 87.4 ms                                                    | 88.9 ms: 1.02x slower                                                         |
| tomli_loads         | 2.12 sec                                                   | 2.18 sec: 1.03x slower                                                        |
| Geometric mean      | (ref)                                                      | 1.01x faster                                                                  |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_process, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                         |
| python_startup_no_site | 7.11 ms                                                    | 7.06 ms: 1.01x faster                                                         |
| Geometric mean         | (ref)                                                      | 1.02x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                         |
| django_template | 34.8 ms                                                    | 35.0 ms: 1.01x slower                                                         |
| genshi_text     | 23.7 ms                                                    | 23.9 ms: 1.01x slower                                                         |
| genshi_xml      | 51.6 ms                                                    | 52.9 ms: 1.03x slower                                                         |
| Geometric mean  | (ref)                                                      | 1.00x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 115 us: 1.43x faster                                                          |
| richards_super             | 57.4 ms                                                    | 52.9 ms: 1.08x faster                                                         |
| richards                   | 50.9 ms                                                    | 47.1 ms: 1.08x faster                                                         |
| mdp                        | 2.79 sec                                                   | 2.58 sec: 1.08x faster                                                        |
| crypto_pyaes               | 77.5 ms                                                    | 72.9 ms: 1.06x faster                                                         |
| pickle_dict                | 34.8 us                                                    | 32.7 us: 1.06x faster                                                         |
| async_tree_none            | 378 ms                                                     | 358 ms: 1.06x faster                                                          |
| unpickle_list              | 5.34 us                                                    | 5.08 us: 1.05x faster                                                         |
| pyflate                    | 484 ms                                                     | 461 ms: 1.05x faster                                                          |
| deepcopy_reduce            | 3.35 us                                                    | 3.19 us: 1.05x faster                                                         |
| scimark_fft                | 392 ms                                                     | 374 ms: 1.05x faster                                                          |
| json_loads                 | 28.9 us                                                    | 27.5 us: 1.05x faster                                                         |
| pickle_list                | 5.11 us                                                    | 4.89 us: 1.04x faster                                                         |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                         |
| raytrace                   | 267 ms                                                     | 257 ms: 1.04x faster                                                          |
| nbody                      | 88.3 ms                                                    | 85.0 ms: 1.04x faster                                                         |
| deepcopy_memo              | 39.7 us                                                    | 38.4 us: 1.04x faster                                                         |
| coroutines                 | 23.2 ms                                                    | 22.4 ms: 1.03x faster                                                         |
| json                       | 5.31 ms                                                    | 5.14 ms: 1.03x faster                                                         |
| spectral_norm              | 116 ms                                                     | 113 ms: 1.03x faster                                                          |
| deepcopy                   | 367 us                                                     | 356 us: 1.03x faster                                                          |
| mako                       | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                         |
| fannkuch                   | 402 ms                                                     | 390 ms: 1.03x faster                                                          |
| scimark_lu                 | 122 ms                                                     | 118 ms: 1.03x faster                                                          |
| gc_traversal               | 3.98 ms                                                    | 3.88 ms: 1.03x faster                                                         |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                         |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                         |
| pickle_pure_python         | 305 us                                                     | 299 us: 1.02x faster                                                          |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                         |
| float                      | 78.9 ms                                                    | 77.2 ms: 1.02x faster                                                         |
| unpickle                   | 15.1 us                                                    | 14.8 us: 1.02x faster                                                         |
| scimark_sor                | 127 ms                                                     | 125 ms: 1.02x faster                                                          |
| chaos                      | 61.3 ms                                                    | 60.2 ms: 1.02x faster                                                         |
| sqlite_synth               | 2.99 us                                                    | 2.93 us: 1.02x faster                                                         |
| dulwich_log                | 67.2 ms                                                    | 66.1 ms: 1.02x faster                                                         |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.2 ms: 1.01x faster                                                         |
| go                         | 145 ms                                                     | 143 ms: 1.01x faster                                                          |
| 2to3                       | 274 ms                                                     | 271 ms: 1.01x faster                                                          |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                         |
| regex_compile              | 137 ms                                                     | 135 ms: 1.01x faster                                                          |
| logging_format             | 6.47 us                                                    | 6.40 us: 1.01x faster                                                         |
| deltablue                  | 3.25 ms                                                    | 3.22 ms: 1.01x faster                                                         |
| logging_silent             | 105 ns                                                     | 104 ns: 1.01x faster                                                          |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                         |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                         |
| thrift                     | 823 us                                                     | 817 us: 1.01x faster                                                          |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                          |
| asyncio_tcp                | 508 ms                                                     | 505 ms: 1.01x faster                                                          |
| python_startup_no_site     | 7.11 ms                                                    | 7.06 ms: 1.01x faster                                                         |
| tornado_http               | 94.6 ms                                                    | 94.1 ms: 1.01x faster                                                         |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.83 sec: 1.00x faster                                                        |
| pidigits                   | 191 ms                                                     | 191 ms: 1.00x faster                                                          |
| bench_thread_pool          | 834 us                                                     | 837 us: 1.00x slower                                                          |
| nqueens                    | 81.4 ms                                                    | 81.8 ms: 1.00x slower                                                         |
| docutils                   | 2.83 sec                                                   | 2.84 sec: 1.00x slower                                                        |
| logging_simple             | 5.74 us                                                    | 5.77 us: 1.00x slower                                                         |
| sympy_sum                  | 156 ms                                                     | 157 ms: 1.01x slower                                                          |
| async_generators           | 442 ms                                                     | 445 ms: 1.01x slower                                                          |
| meteor_contest             | 110 ms                                                     | 110 ms: 1.01x slower                                                          |
| django_template            | 34.8 ms                                                    | 35.0 ms: 1.01x slower                                                         |
| sqlglot_normalize          | 110 ms                                                     | 111 ms: 1.01x slower                                                          |
| hexiom                     | 6.30 ms                                                    | 6.35 ms: 1.01x slower                                                         |
| comprehensions             | 16.6 us                                                    | 16.8 us: 1.01x slower                                                         |
| xml_etree_iterparse        | 107 ms                                                     | 108 ms: 1.01x slower                                                          |
| pprint_pformat             | 1.56 sec                                                   | 1.57 sec: 1.01x slower                                                        |
| pprint_safe_repr           | 758 ms                                                     | 766 ms: 1.01x slower                                                          |
| regex_v8                   | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                         |
| genshi_text                | 23.7 ms                                                    | 23.9 ms: 1.01x slower                                                         |
| pathlib                    | 17.3 ms                                                    | 17.5 ms: 1.01x slower                                                         |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                         |
| xml_etree_generate         | 87.4 ms                                                    | 88.9 ms: 1.02x slower                                                         |
| regex_effbot               | 3.67 ms                                                    | 3.74 ms: 1.02x slower                                                         |
| genshi_xml                 | 51.6 ms                                                    | 52.9 ms: 1.03x slower                                                         |
| generators                 | 29.6 ms                                                    | 30.4 ms: 1.03x slower                                                         |
| tomli_loads                | 2.12 sec                                                   | 2.18 sec: 1.03x slower                                                        |
| telco                      | 8.41 ms                                                    | 8.69 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 607 ms: 1.03x slower                                                          |
| coverage                   | 93.1 ms                                                    | 97.9 ms: 1.05x slower                                                         |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                  |

Benchmark hidden because not significant (23): async_tree_io, html5lib, xml_etree_parse, mypy2, async_tree_memoization, xml_etree_process, chameleon, scimark_sparse_mat_mult, dask, sqlglot_optimize, pycparser, bench_mp_pool, sympy_str, sympy_integrate, regex_dna, async_tree_io_tg, async_tree_memoization_tg, unpickle_pure_python, sympy_expand, async_tree_none_tg, async_tree_cpu_io_mixed, pylint, djangocms
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 96.77% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x