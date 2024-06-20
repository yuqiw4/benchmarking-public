# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: exits
- machine: linux-x86_64
- commit hash: b9f3875
- commit date: 2024-05-02
- overall geometric mean: 1.00x faster
- HPT reliability: 90.07%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 280 ms: 1.02x slower                                          |
| chameleon      | 7.22 ms                                                    | 7.05 ms: 1.02x faster                                         |
| docutils       | 2.83 sec                                                   | 2.93 sec: 1.04x slower                                        |
| html5lib       | 67.2 ms                                                    | 66.6 ms: 1.01x faster                                         |
| tornado_http   | 94.6 ms                                                    | 96.2 ms: 1.02x slower                                         |
| Geometric mean | (ref)                                                      | 1.01x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 355 ms: 1.07x faster                                          |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 608 ms: 1.04x slower                                          |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                  |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 80.0 ms: 1.10x faster                                         |
| float          | 78.9 ms                                                    | 73.5 ms: 1.07x faster                                         |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                          |
| Geometric mean | (ref)                                                      | 1.06x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.1 ms: 1.04x faster                                         |
| regex_effbot   | 3.67 ms                                                    | 3.60 ms: 1.02x faster                                         |
| regex_dna      | 221 ms                                                     | 223 ms: 1.01x slower                                          |
| regex_compile  | 137 ms                                                     | 139 ms: 1.01x slower                                          |
| Geometric mean | (ref)                                                      | 1.01x faster                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|---------------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| tomli_loads         | 2.12 sec                                                   | 1.92 sec: 1.10x faster                                        |
| xml_etree_parse     | 162 ms                                                     | 150 ms: 1.08x faster                                          |
| xml_etree_iterparse | 107 ms                                                     | 101 ms: 1.07x faster                                          |
| json_loads          | 28.9 us                                                    | 27.5 us: 1.05x faster                                         |
| xml_etree_process   | 61.2 ms                                                    | 59.3 ms: 1.03x faster                                         |
| json_dumps          | 10.7 ms                                                    | 10.5 ms: 1.03x faster                                         |
| pickle_list         | 5.11 us                                                    | 4.99 us: 1.02x faster                                         |
| xml_etree_generate  | 87.4 ms                                                    | 86.6 ms: 1.01x faster                                         |
| unpickle_list       | 5.34 us                                                    | 5.30 us: 1.01x faster                                         |
| pickle_dict         | 34.8 us                                                    | 34.7 us: 1.00x faster                                         |
| pickle_pure_python  | 305 us                                                     | 307 us: 1.01x slower                                          |
| pickle              | 11.5 us                                                    | 11.9 us: 1.03x slower                                         |
| unpickle            | 15.1 us                                                    | 16.1 us: 1.07x slower                                         |
| Geometric mean      | (ref)                                                      | 1.02x faster                                                  |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                         |
| python_startup_no_site | 7.11 ms                                                    | 7.60 ms: 1.07x slower                                         |
| Geometric mean         | (ref)                                                      | 1.05x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|-----------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 9.69 ms: 1.16x faster                                         |
| django_template | 34.8 ms                                                    | 36.9 ms: 1.06x slower                                         |
| genshi_text     | 23.7 ms                                                    | 25.4 ms: 1.07x slower                                         |
| genshi_xml      | 51.6 ms                                                    | 59.3 ms: 1.15x slower                                         |
| Geometric mean  | (ref)                                                      | 1.03x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------:|
| scimark_fft                | 392 ms                                                     | 314 ms: 1.25x faster                                          |
| spectral_norm              | 116 ms                                                     | 94.8 ms: 1.23x faster                                         |
| richards                   | 50.9 ms                                                    | 42.3 ms: 1.20x faster                                         |
| richards_super             | 57.4 ms                                                    | 49.0 ms: 1.17x faster                                         |
| mako                       | 11.2 ms                                                    | 9.69 ms: 1.16x faster                                         |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.55 ms: 1.16x faster                                         |
| fannkuch                   | 402 ms                                                     | 349 ms: 1.15x faster                                          |
| crypto_pyaes               | 77.5 ms                                                    | 70.1 ms: 1.10x faster                                         |
| tomli_loads                | 2.12 sec                                                   | 1.92 sec: 1.10x faster                                        |
| nbody                      | 88.3 ms                                                    | 80.0 ms: 1.10x faster                                         |
| xml_etree_parse            | 162 ms                                                     | 150 ms: 1.08x faster                                          |
| mdp                        | 2.79 sec                                                   | 2.59 sec: 1.08x faster                                        |
| float                      | 78.9 ms                                                    | 73.5 ms: 1.07x faster                                         |
| scimark_monte_carlo        | 69.2 ms                                                    | 64.6 ms: 1.07x faster                                         |
| pyflate                    | 484 ms                                                     | 453 ms: 1.07x faster                                          |
| xml_etree_iterparse        | 107 ms                                                     | 101 ms: 1.07x faster                                          |
| async_tree_none            | 378 ms                                                     | 355 ms: 1.07x faster                                          |
| logging_silent             | 105 ns                                                     | 99.1 ns: 1.06x faster                                         |
| json_loads                 | 28.9 us                                                    | 27.5 us: 1.05x faster                                         |
| sqlite_synth               | 2.99 us                                                    | 2.86 us: 1.05x faster                                         |
| json                       | 5.31 ms                                                    | 5.09 ms: 1.04x faster                                         |
| gc_traversal               | 3.98 ms                                                    | 3.81 ms: 1.04x faster                                         |
| regex_v8                   | 25.1 ms                                                    | 24.1 ms: 1.04x faster                                         |
| pprint_safe_repr           | 758 ms                                                     | 731 ms: 1.04x faster                                          |
| deepcopy_reduce            | 3.35 us                                                    | 3.24 us: 1.03x faster                                         |
| xml_etree_process          | 61.2 ms                                                    | 59.3 ms: 1.03x faster                                         |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.03x faster                                         |
| chameleon                  | 7.22 ms                                                    | 7.05 ms: 1.02x faster                                         |
| pickle_list                | 5.11 us                                                    | 4.99 us: 1.02x faster                                         |
| create_gc_cycles           | 1.82 ms                                                    | 1.78 ms: 1.02x faster                                         |
| regex_effbot               | 3.67 ms                                                    | 3.60 ms: 1.02x faster                                         |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                         |
| pprint_pformat             | 1.56 sec                                                   | 1.53 sec: 1.02x faster                                        |
| logging_format             | 6.47 us                                                    | 6.37 us: 1.02x faster                                         |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                          |
| thrift                     | 823 us                                                     | 814 us: 1.01x faster                                          |
| xml_etree_generate         | 87.4 ms                                                    | 86.6 ms: 1.01x faster                                         |
| html5lib                   | 67.2 ms                                                    | 66.6 ms: 1.01x faster                                         |
| chaos                      | 61.3 ms                                                    | 60.8 ms: 1.01x faster                                         |
| unpickle_list              | 5.34 us                                                    | 5.30 us: 1.01x faster                                         |
| pickle_dict                | 34.8 us                                                    | 34.7 us: 1.00x faster                                         |
| pickle_pure_python         | 305 us                                                     | 307 us: 1.01x slower                                          |
| meteor_contest             | 110 ms                                                     | 110 ms: 1.01x slower                                          |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                        |
| sqlglot_transpile          | 1.63 ms                                                    | 1.65 ms: 1.01x slower                                         |
| comprehensions             | 16.6 us                                                    | 16.8 us: 1.01x slower                                         |
| regex_dna                  | 221 ms                                                     | 223 ms: 1.01x slower                                          |
| logging_simple             | 5.74 us                                                    | 5.81 us: 1.01x slower                                         |
| regex_compile              | 137 ms                                                     | 139 ms: 1.01x slower                                          |
| telco                      | 8.41 ms                                                    | 8.55 ms: 1.02x slower                                         |
| pycparser                  | 1.16 sec                                                   | 1.18 sec: 1.02x slower                                        |
| tornado_http               | 94.6 ms                                                    | 96.2 ms: 1.02x slower                                         |
| dask                       | 369 ms                                                     | 378 ms: 1.02x slower                                          |
| 2to3                       | 274 ms                                                     | 280 ms: 1.02x slower                                          |
| generators                 | 29.6 ms                                                    | 30.3 ms: 1.02x slower                                         |
| djangocms                  | 31.5 us                                                    | 32.3 us: 1.02x slower                                         |
| python_startup             | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                         |
| gunicorn                   | 1.28 ms                                                    | 1.31 ms: 1.03x slower                                         |
| dulwich_log                | 67.2 ms                                                    | 69.2 ms: 1.03x slower                                         |
| raytrace                   | 267 ms                                                     | 275 ms: 1.03x slower                                          |
| sqlglot_optimize           | 55.5 ms                                                    | 57.3 ms: 1.03x slower                                         |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.03x slower                                         |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 608 ms: 1.04x slower                                          |
| docutils                   | 2.83 sec                                                   | 2.93 sec: 1.04x slower                                        |
| pathlib                    | 17.3 ms                                                    | 18.0 ms: 1.04x slower                                         |
| bench_thread_pool          | 834 us                                                     | 864 us: 1.04x slower                                          |
| aiohttp                    | 1.18 ms                                                    | 1.22 ms: 1.04x slower                                         |
| scimark_lu                 | 122 ms                                                     | 127 ms: 1.04x slower                                          |
| sqlglot_normalize          | 110 ms                                                     | 115 ms: 1.05x slower                                          |
| asyncio_tcp                | 508 ms                                                     | 532 ms: 1.05x slower                                          |
| hexiom                     | 6.30 ms                                                    | 6.62 ms: 1.05x slower                                         |
| sympy_str                  | 282 ms                                                     | 297 ms: 1.05x slower                                          |
| async_generators           | 442 ms                                                     | 466 ms: 1.05x slower                                          |
| typing_runtime_protocols   | 165 us                                                     | 174 us: 1.06x slower                                          |
| django_template            | 34.8 ms                                                    | 36.9 ms: 1.06x slower                                         |
| go                         | 145 ms                                                     | 154 ms: 1.06x slower                                          |
| unpickle                   | 15.1 us                                                    | 16.1 us: 1.07x slower                                         |
| python_startup_no_site     | 7.11 ms                                                    | 7.60 ms: 1.07x slower                                         |
| genshi_text                | 23.7 ms                                                    | 25.4 ms: 1.07x slower                                         |
| sympy_expand               | 473 ms                                                     | 507 ms: 1.07x slower                                          |
| sympy_sum                  | 156 ms                                                     | 168 ms: 1.08x slower                                          |
| scimark_sor                | 127 ms                                                     | 138 ms: 1.08x slower                                          |
| sympy_integrate            | 20.5 ms                                                    | 22.3 ms: 1.09x slower                                         |
| nqueens                    | 81.4 ms                                                    | 89.0 ms: 1.09x slower                                         |
| mypy2                      | 742 ms                                                     | 818 ms: 1.10x slower                                          |
| pylint                     | 317 ms                                                     | 353 ms: 1.11x slower                                          |
| genshi_xml                 | 51.6 ms                                                    | 59.3 ms: 1.15x slower                                         |
| deltablue                  | 3.25 ms                                                    | 3.76 ms: 1.16x slower                                         |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                  |

Benchmark hidden because not significant (13): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, asyncio_websockets, unpickle_pure_python, sqlglot_parse, coverage, deepcopy, async_tree_memoization, deepcopy_memo, bench_mp_pool, async_tree_cpu_io_mixed, async_tree_io_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 90.07% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x