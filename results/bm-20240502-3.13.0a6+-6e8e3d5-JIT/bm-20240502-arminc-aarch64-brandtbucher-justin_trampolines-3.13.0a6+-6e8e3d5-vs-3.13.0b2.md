# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_trampolines
- machine: linux-aarch64
- commit hash: 6e8e3d5
- commit date: 2024-05-02
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 305 ms                                                       | 351 ms: 1.15x slower                                                         |
| chameleon      | 8.95 ms                                                      | 9.40 ms: 1.05x slower                                                        |
| docutils       | 3.10 sec                                                     | 3.43 sec: 1.11x slower                                                       |
| html5lib       | 66.1 ms                                                      | 71.0 ms: 1.08x slower                                                        |
| tornado_http   | 128 ms                                                       | 139 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                        | 1.09x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg        | 1.27 sec                                                     | 1.19 sec: 1.07x faster                                                       |
| async_tree_cpu_io_mixed | 791 ms                                                       | 807 ms: 1.02x slower                                                         |
| async_tree_none         | 492 ms                                                       | 510 ms: 1.04x slower                                                         |
| Geometric mean          | (ref)                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_io, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 114 ms                                                       | 106 ms: 1.08x faster                                                         |
| float          | 91.4 ms                                                      | 88.5 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                        | 1.04x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 31.1 ms                                                      | 30.3 ms: 1.03x faster                                                        |
| regex_dna      | 259 ms                                                       | 254 ms: 1.02x faster                                                         |
| regex_effbot   | 4.98 ms                                                      | 4.91 ms: 1.01x faster                                                        |
| regex_compile  | 128 ms                                                       | 163 ms: 1.27x slower                                                         |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_list        | 6.52 us                                                      | 6.41 us: 1.02x faster                                                        |
| unpickle             | 19.8 us                                                      | 19.6 us: 1.01x faster                                                        |
| json_loads           | 32.1 us                                                      | 31.9 us: 1.01x faster                                                        |
| pickle_list          | 5.27 us                                                      | 5.34 us: 1.01x slower                                                        |
| pickle               | 13.4 us                                                      | 13.6 us: 1.01x slower                                                        |
| unpickle_pure_python | 251 us                                                       | 279 us: 1.11x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (8): xml_etree_parse, xml_etree_process, tomli_loads, json_dumps, pickle_dict, xml_etree_iterparse, xml_etree_generate, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.0 ms                                                      | 14.7 ms: 1.13x slower                                                        |
| python_startup_no_site | 8.60 ms                                                      | 10.7 ms: 1.24x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.19x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 13.2 ms                                                      | 12.8 ms: 1.03x faster                                                        |
| django_template | 42.3 ms                                                      | 50.6 ms: 1.20x slower                                                        |
| genshi_text     | 27.4 ms                                                      | 34.5 ms: 1.26x slower                                                        |
| genshi_xml      | 60.4 ms                                                      | 80.3 ms: 1.33x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.18x slower                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-arminc-aarch64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody                    | 114 ms                                                       | 106 ms: 1.08x faster                                                         |
| async_tree_io_tg         | 1.27 sec                                                     | 1.19 sec: 1.07x faster                                                       |
| richards                 | 55.9 ms                                                      | 53.3 ms: 1.05x faster                                                        |
| gc_traversal             | 5.17 ms                                                      | 4.96 ms: 1.04x faster                                                        |
| richards_super           | 62.3 ms                                                      | 60.2 ms: 1.04x faster                                                        |
| telco                    | 10.0 ms                                                      | 9.69 ms: 1.03x faster                                                        |
| float                    | 91.4 ms                                                      | 88.5 ms: 1.03x faster                                                        |
| mako                     | 13.2 ms                                                      | 12.8 ms: 1.03x faster                                                        |
| regex_v8                 | 31.1 ms                                                      | 30.3 ms: 1.03x faster                                                        |
| regex_dna                | 259 ms                                                       | 254 ms: 1.02x faster                                                         |
| sqlite_synth             | 3.90 us                                                      | 3.84 us: 1.02x faster                                                        |
| unpickle_list            | 6.52 us                                                      | 6.41 us: 1.02x faster                                                        |
| regex_effbot             | 4.98 ms                                                      | 4.91 ms: 1.01x faster                                                        |
| spectral_norm            | 141 ms                                                       | 139 ms: 1.01x faster                                                         |
| unpickle                 | 19.8 us                                                      | 19.6 us: 1.01x faster                                                        |
| json_loads               | 32.1 us                                                      | 31.9 us: 1.01x faster                                                        |
| scimark_fft              | 445 ms                                                       | 449 ms: 1.01x slower                                                         |
| fannkuch                 | 451 ms                                                       | 456 ms: 1.01x slower                                                         |
| pickle_list              | 5.27 us                                                      | 5.34 us: 1.01x slower                                                        |
| asyncio_tcp_ssl          | 2.21 sec                                                     | 2.24 sec: 1.01x slower                                                       |
| pickle                   | 13.4 us                                                      | 13.6 us: 1.01x slower                                                        |
| coverage                 | 98.4 ms                                                      | 100 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed  | 791 ms                                                       | 807 ms: 1.02x slower                                                         |
| generators               | 37.1 ms                                                      | 38.2 ms: 1.03x slower                                                        |
| mdp                      | 3.33 sec                                                     | 3.43 sec: 1.03x slower                                                       |
| deepcopy                 | 448 us                                                       | 463 us: 1.03x slower                                                         |
| scimark_monte_carlo      | 82.3 ms                                                      | 85.1 ms: 1.03x slower                                                        |
| async_tree_none          | 492 ms                                                       | 510 ms: 1.04x slower                                                         |
| async_generators         | 488 ms                                                       | 506 ms: 1.04x slower                                                         |
| deepcopy_reduce          | 4.04 us                                                      | 4.19 us: 1.04x slower                                                        |
| coroutines               | 29.0 ms                                                      | 30.1 ms: 1.04x slower                                                        |
| logging_format           | 7.82 us                                                      | 8.19 us: 1.05x slower                                                        |
| logging_simple           | 7.21 us                                                      | 7.55 us: 1.05x slower                                                        |
| chameleon                | 8.95 ms                                                      | 9.40 ms: 1.05x slower                                                        |
| scimark_sparse_mat_mult  | 6.55 ms                                                      | 6.90 ms: 1.05x slower                                                        |
| meteor_contest           | 113 ms                                                       | 120 ms: 1.06x slower                                                         |
| sqlglot_parse            | 1.42 ms                                                      | 1.51 ms: 1.06x slower                                                        |
| bench_thread_pool        | 1.26 ms                                                      | 1.33 ms: 1.06x slower                                                        |
| pycparser                | 1.22 sec                                                     | 1.30 sec: 1.06x slower                                                       |
| asyncio_tcp              | 584 ms                                                       | 621 ms: 1.06x slower                                                         |
| raytrace                 | 297 ms                                                       | 317 ms: 1.07x slower                                                         |
| sqlglot_normalize        | 129 ms                                                       | 139 ms: 1.07x slower                                                         |
| crypto_pyaes             | 82.0 ms                                                      | 88.1 ms: 1.07x slower                                                        |
| html5lib                 | 66.1 ms                                                      | 71.0 ms: 1.08x slower                                                        |
| pyflate                  | 557 ms                                                       | 600 ms: 1.08x slower                                                         |
| dask                     | 370 ms                                                       | 401 ms: 1.08x slower                                                         |
| tornado_http             | 128 ms                                                       | 139 ms: 1.08x slower                                                         |
| typing_runtime_protocols | 193 us                                                       | 211 us: 1.09x slower                                                         |
| sqlglot_optimize         | 62.6 ms                                                      | 68.9 ms: 1.10x slower                                                        |
| sqlglot_transpile        | 1.71 ms                                                      | 1.89 ms: 1.10x slower                                                        |
| docutils                 | 3.10 sec                                                     | 3.43 sec: 1.11x slower                                                       |
| unpickle_pure_python     | 251 us                                                       | 279 us: 1.11x slower                                                         |
| bench_mp_pool            | 7.03 ms                                                      | 7.91 ms: 1.12x slower                                                        |
| python_startup           | 13.0 ms                                                      | 14.7 ms: 1.13x slower                                                        |
| go                       | 161 ms                                                       | 185 ms: 1.15x slower                                                         |
| comprehensions           | 20.5 us                                                      | 23.6 us: 1.15x slower                                                        |
| sympy_expand             | 457 ms                                                       | 527 ms: 1.15x slower                                                         |
| 2to3                     | 305 ms                                                       | 351 ms: 1.15x slower                                                         |
| scimark_sor              | 159 ms                                                       | 184 ms: 1.16x slower                                                         |
| sympy_str                | 265 ms                                                       | 310 ms: 1.17x slower                                                         |
| deltablue                | 3.88 ms                                                      | 4.62 ms: 1.19x slower                                                        |
| django_template          | 42.3 ms                                                      | 50.6 ms: 1.20x slower                                                        |
| nqueens                  | 98.9 ms                                                      | 120 ms: 1.21x slower                                                         |
| dulwich_log              | 58.5 ms                                                      | 71.3 ms: 1.22x slower                                                        |
| pylint                   | 337 ms                                                       | 413 ms: 1.23x slower                                                         |
| sympy_integrate          | 20.9 ms                                                      | 25.9 ms: 1.24x slower                                                        |
| python_startup_no_site   | 8.60 ms                                                      | 10.7 ms: 1.24x slower                                                        |
| sympy_sum                | 144 ms                                                       | 179 ms: 1.24x slower                                                         |
| pprint_safe_repr         | 933 ms                                                       | 1.17 sec: 1.25x slower                                                       |
| pprint_pformat           | 1.93 sec                                                     | 2.42 sec: 1.25x slower                                                       |
| chaos                    | 68.3 ms                                                      | 85.7 ms: 1.26x slower                                                        |
| genshi_text              | 27.4 ms                                                      | 34.5 ms: 1.26x slower                                                        |
| hexiom                   | 7.08 ms                                                      | 8.97 ms: 1.27x slower                                                        |
| regex_compile            | 128 ms                                                       | 163 ms: 1.27x slower                                                         |
| scimark_lu               | 141 ms                                                       | 180 ms: 1.27x slower                                                         |
| genshi_xml               | 60.4 ms                                                      | 80.3 ms: 1.33x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.06x slower                                                                 |

Benchmark hidden because not significant (21): xml_etree_parse, create_gc_cycles, xml_etree_process, async_tree_none_tg, pidigits, async_tree_io, tomli_loads, logging_silent, json_dumps, pickle_dict, xml_etree_iterparse, xml_etree_generate, deepcopy_memo, asyncio_websockets, pathlib, thrift, pickle_pure_python, json, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization
Ignored benchmarks (5) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17.json: aiohttp, bpe_tokeniser, flaskblogging, gunicorn, mypy2

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.07x