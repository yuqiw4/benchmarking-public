# Results vs. 3.13.0b2

- fork: python
- ref: main
- machine: linux-aarch64
- commit hash: a7711a2
- commit date: 2024-05-01
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 305 ms                                                       | 348 ms: 1.14x slower                                     |
| chameleon      | 8.95 ms                                                      | 9.13 ms: 1.02x slower                                    |
| docutils       | 3.10 sec                                                     | 3.41 sec: 1.10x slower                                   |
| html5lib       | 66.1 ms                                                      | 70.3 ms: 1.06x slower                                    |
| tornado_http   | 128 ms                                                       | 139 ms: 1.08x slower                                     |
| Geometric mean | (ref)                                                        | 1.08x slower                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|-------------------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_io_tg        | 1.27 sec                                                     | 1.20 sec: 1.06x faster                                   |
| async_tree_cpu_io_mixed | 791 ms                                                       | 809 ms: 1.02x slower                                     |
| async_tree_none         | 492 ms                                                       | 511 ms: 1.04x slower                                     |
| Geometric mean          | (ref)                                                        | 1.01x slower                                             |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| nbody          | 114 ms                                                       | 108 ms: 1.06x faster                                     |
| float          | 91.4 ms                                                      | 90.3 ms: 1.01x faster                                    |
| pidigits       | 234 ms                                                       | 233 ms: 1.01x faster                                     |
| Geometric mean | (ref)                                                        | 1.03x faster                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna      | 259 ms                                                       | 246 ms: 1.05x faster                                     |
| regex_effbot   | 4.98 ms                                                      | 4.84 ms: 1.03x faster                                    |
| regex_v8       | 31.1 ms                                                      | 30.3 ms: 1.03x faster                                    |
| regex_compile  | 128 ms                                                       | 159 ms: 1.24x slower                                     |
| Geometric mean | (ref)                                                        | 1.03x slower                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| json_dumps           | 13.1 ms                                                      | 12.9 ms: 1.02x faster                                    |
| json_loads           | 32.1 us                                                      | 31.8 us: 1.01x faster                                    |
| tomli_loads          | 2.57 sec                                                     | 2.56 sec: 1.00x faster                                   |
| xml_etree_iterparse  | 147 ms                                                       | 148 ms: 1.01x slower                                     |
| pickle               | 13.4 us                                                      | 13.5 us: 1.01x slower                                    |
| unpickle_pure_python | 251 us                                                       | 277 us: 1.10x slower                                     |
| Geometric mean       | (ref)                                                        | 1.00x slower                                             |

Benchmark hidden because not significant (8): xml_etree_parse, pickle_pure_python, unpickle_list, xml_etree_process, pickle_list, xml_etree_generate, unpickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 13.0 ms                                                      | 14.7 ms: 1.13x slower                                    |
| python_startup_no_site | 8.60 ms                                                      | 10.7 ms: 1.24x slower                                    |
| Geometric mean         | (ref)                                                        | 1.18x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| mako            | 13.2 ms                                                      | 13.0 ms: 1.01x faster                                    |
| django_template | 42.3 ms                                                      | 48.5 ms: 1.15x slower                                    |
| genshi_text     | 27.4 ms                                                      | 33.6 ms: 1.23x slower                                    |
| genshi_xml      | 60.4 ms                                                      | 78.3 ms: 1.30x slower                                    |
| Geometric mean  | (ref)                                                        | 1.16x slower                                             |

All benchmarks:
===============

| Benchmark                | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------:|
| richards                 | 55.9 ms                                                      | 52.3 ms: 1.07x faster                                    |
| async_tree_io_tg         | 1.27 sec                                                     | 1.20 sec: 1.06x faster                                   |
| nbody                    | 114 ms                                                       | 108 ms: 1.06x faster                                     |
| regex_dna                | 259 ms                                                       | 246 ms: 1.05x faster                                     |
| richards_super           | 62.3 ms                                                      | 59.4 ms: 1.05x faster                                    |
| regex_effbot             | 4.98 ms                                                      | 4.84 ms: 1.03x faster                                    |
| regex_v8                 | 31.1 ms                                                      | 30.3 ms: 1.03x faster                                    |
| gc_traversal             | 5.17 ms                                                      | 5.05 ms: 1.02x faster                                    |
| json_dumps               | 13.1 ms                                                      | 12.9 ms: 1.02x faster                                    |
| mako                     | 13.2 ms                                                      | 13.0 ms: 1.01x faster                                    |
| telco                    | 10.0 ms                                                      | 9.88 ms: 1.01x faster                                    |
| float                    | 91.4 ms                                                      | 90.3 ms: 1.01x faster                                    |
| sqlite_synth             | 3.90 us                                                      | 3.85 us: 1.01x faster                                    |
| json_loads               | 32.1 us                                                      | 31.8 us: 1.01x faster                                    |
| pidigits                 | 234 ms                                                       | 233 ms: 1.01x faster                                     |
| tomli_loads              | 2.57 sec                                                     | 2.56 sec: 1.00x faster                                   |
| spectral_norm            | 141 ms                                                       | 142 ms: 1.01x slower                                     |
| coverage                 | 98.4 ms                                                      | 99.2 ms: 1.01x slower                                    |
| xml_etree_iterparse      | 147 ms                                                       | 148 ms: 1.01x slower                                     |
| pickle                   | 13.4 us                                                      | 13.5 us: 1.01x slower                                    |
| deepcopy_reduce          | 4.04 us                                                      | 4.11 us: 1.02x slower                                    |
| fannkuch                 | 451 ms                                                       | 460 ms: 1.02x slower                                     |
| chameleon                | 8.95 ms                                                      | 9.13 ms: 1.02x slower                                    |
| scimark_fft              | 445 ms                                                       | 454 ms: 1.02x slower                                     |
| pathlib                  | 22.8 ms                                                      | 23.3 ms: 1.02x slower                                    |
| async_tree_cpu_io_mixed  | 791 ms                                                       | 809 ms: 1.02x slower                                     |
| asyncio_tcp_ssl          | 2.21 sec                                                     | 2.26 sec: 1.02x slower                                   |
| generators               | 37.1 ms                                                      | 38.1 ms: 1.03x slower                                    |
| async_generators         | 488 ms                                                       | 501 ms: 1.03x slower                                     |
| deepcopy                 | 448 us                                                       | 460 us: 1.03x slower                                     |
| scimark_monte_carlo      | 82.3 ms                                                      | 84.8 ms: 1.03x slower                                    |
| mdp                      | 3.33 sec                                                     | 3.44 sec: 1.03x slower                                   |
| coroutines               | 29.0 ms                                                      | 30.0 ms: 1.04x slower                                    |
| async_tree_none          | 492 ms                                                       | 511 ms: 1.04x slower                                     |
| bench_thread_pool        | 1.26 ms                                                      | 1.31 ms: 1.04x slower                                    |
| pycparser                | 1.22 sec                                                     | 1.28 sec: 1.05x slower                                   |
| asyncio_tcp              | 584 ms                                                       | 614 ms: 1.05x slower                                     |
| meteor_contest           | 113 ms                                                       | 120 ms: 1.06x slower                                     |
| logging_format           | 7.82 us                                                      | 8.27 us: 1.06x slower                                    |
| sqlglot_normalize        | 129 ms                                                       | 137 ms: 1.06x slower                                     |
| bench_mp_pool            | 7.03 ms                                                      | 7.46 ms: 1.06x slower                                    |
| logging_simple           | 7.21 us                                                      | 7.65 us: 1.06x slower                                    |
| html5lib                 | 66.1 ms                                                      | 70.3 ms: 1.06x slower                                    |
| crypto_pyaes             | 82.0 ms                                                      | 87.2 ms: 1.06x slower                                    |
| sqlglot_parse            | 1.42 ms                                                      | 1.52 ms: 1.07x slower                                    |
| raytrace                 | 297 ms                                                       | 316 ms: 1.07x slower                                     |
| dask                     | 370 ms                                                       | 397 ms: 1.07x slower                                     |
| scimark_sparse_mat_mult  | 6.55 ms                                                      | 7.02 ms: 1.07x slower                                    |
| pyflate                  | 557 ms                                                       | 598 ms: 1.07x slower                                     |
| tornado_http             | 128 ms                                                       | 139 ms: 1.08x slower                                     |
| sqlglot_optimize         | 62.6 ms                                                      | 68.1 ms: 1.09x slower                                    |
| docutils                 | 3.10 sec                                                     | 3.41 sec: 1.10x slower                                   |
| sqlglot_transpile        | 1.71 ms                                                      | 1.89 ms: 1.10x slower                                    |
| unpickle_pure_python     | 251 us                                                       | 277 us: 1.10x slower                                     |
| typing_runtime_protocols | 193 us                                                       | 215 us: 1.11x slower                                     |
| python_startup           | 13.0 ms                                                      | 14.7 ms: 1.13x slower                                    |
| sympy_expand             | 457 ms                                                       | 519 ms: 1.14x slower                                     |
| scimark_sor              | 159 ms                                                       | 181 ms: 1.14x slower                                     |
| comprehensions           | 20.5 us                                                      | 23.4 us: 1.14x slower                                    |
| 2to3                     | 305 ms                                                       | 348 ms: 1.14x slower                                     |
| django_template          | 42.3 ms                                                      | 48.5 ms: 1.15x slower                                    |
| sympy_str                | 265 ms                                                       | 306 ms: 1.15x slower                                     |
| go                       | 161 ms                                                       | 186 ms: 1.16x slower                                     |
| deltablue                | 3.88 ms                                                      | 4.58 ms: 1.18x slower                                    |
| pylint                   | 337 ms                                                       | 406 ms: 1.21x slower                                     |
| dulwich_log              | 58.5 ms                                                      | 70.7 ms: 1.21x slower                                    |
| chaos                    | 68.3 ms                                                      | 82.8 ms: 1.21x slower                                    |
| nqueens                  | 98.9 ms                                                      | 120 ms: 1.21x slower                                     |
| sympy_sum                | 144 ms                                                       | 175 ms: 1.22x slower                                     |
| sympy_integrate          | 20.9 ms                                                      | 25.5 ms: 1.22x slower                                    |
| genshi_text              | 27.4 ms                                                      | 33.6 ms: 1.23x slower                                    |
| python_startup_no_site   | 8.60 ms                                                      | 10.7 ms: 1.24x slower                                    |
| regex_compile            | 128 ms                                                       | 159 ms: 1.24x slower                                     |
| pprint_pformat           | 1.93 sec                                                     | 2.42 sec: 1.25x slower                                   |
| pprint_safe_repr         | 933 ms                                                       | 1.17 sec: 1.25x slower                                   |
| scimark_lu               | 141 ms                                                       | 178 ms: 1.26x slower                                     |
| hexiom                   | 7.08 ms                                                      | 8.94 ms: 1.26x slower                                    |
| genshi_xml               | 60.4 ms                                                      | 78.3 ms: 1.30x slower                                    |
| Geometric mean           | (ref)                                                        | 1.06x slower                                             |

Benchmark hidden because not significant (19): xml_etree_parse, json, deepcopy_memo, pickle_pure_python, create_gc_cycles, unpickle_list, xml_etree_process, async_tree_none_tg, pickle_list, logging_silent, xml_etree_generate, unpickle, pickle_dict, asyncio_websockets, async_tree_io, thrift, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_memoization
Ignored benchmarks (5) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17.json: aiohttp, bpe_tokeniser, flaskblogging, gunicorn, mypy2

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.07x