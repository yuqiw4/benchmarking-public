# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.01x slower
- HPT reliability: 99.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 299 ms: 1.03x slower                                                       |
| chameleon      | 7.40 ms                                                          | 7.29 ms: 1.01x faster                                                      |
| docutils       | 2.98 sec                                                         | 3.08 sec: 1.03x slower                                                     |
| html5lib       | 74.7 ms                                                          | 73.2 ms: 1.02x faster                                                      |
| tornado_http   | 119 ms                                                           | 124 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                            | 1.01x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|---------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization    | 460 ms                                                           | 442 ms: 1.04x faster                                                       |
| async_tree_cpu_io_mixed   | 604 ms                                                           | 596 ms: 1.01x faster                                                       |
| async_tree_io_tg          | 900 ms                                                           | 912 ms: 1.01x slower                                                       |
| async_tree_memoization_tg | 421 ms                                                           | 434 ms: 1.03x slower                                                       |
| Geometric mean            | (ref)                                                            | 1.00x slower                                                               |

Benchmark hidden because not significant (4): async_tree_none, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 77.4 ms: 1.04x faster                                                      |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                            | 1.01x faster                                                               |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 245 ms: 1.02x faster                                                       |
| regex_v8       | 26.0 ms                                                          | 25.9 ms: 1.00x faster                                                      |
| regex_effbot   | 3.40 ms                                                          | 3.45 ms: 1.01x slower                                                      |
| regex_compile  | 144 ms                                                           | 146 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                            | 1.00x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.10 sec: 1.14x faster                                                     |
| unpickle             | 15.7 us                                                          | 14.6 us: 1.08x faster                                                      |
| pickle_dict          | 32.8 us                                                          | 31.1 us: 1.06x faster                                                      |
| xml_etree_process    | 59.7 ms                                                          | 58.1 ms: 1.03x faster                                                      |
| pickle               | 10.6 us                                                          | 10.4 us: 1.02x faster                                                      |
| xml_etree_generate   | 85.7 ms                                                          | 84.0 ms: 1.02x faster                                                      |
| pickle_list          | 4.44 us                                                          | 4.39 us: 1.01x faster                                                      |
| pickle_pure_python   | 307 us                                                           | 305 us: 1.01x faster                                                       |
| xml_etree_iterparse  | 103 ms                                                           | 103 ms: 1.00x slower                                                       |
| json_dumps           | 10.8 ms                                                          | 10.8 ms: 1.01x slower                                                      |
| json_loads           | 25.0 us                                                          | 25.3 us: 1.01x slower                                                      |
| unpickle_pure_python | 224 us                                                           | 229 us: 1.02x slower                                                       |
| xml_etree_parse      | 144 ms                                                           | 147 ms: 1.02x slower                                                       |
| Geometric mean       | (ref)                                                            | 1.02x faster                                                               |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.6 ms: 1.03x slower                                                      |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                      |
| Geometric mean         | (ref)                                                            | 1.17x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 9.27 ms: 1.12x faster                                                      |
| genshi_xml      | 58.1 ms                                                          | 57.3 ms: 1.01x faster                                                      |
| django_template | 39.0 ms                                                          | 39.8 ms: 1.02x slower                                                      |
| genshi_text     | 25.9 ms                                                          | 26.8 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                            | 1.02x faster                                                               |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|---------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols  | 171 us                                                           | 115 us: 1.48x faster                                                       |
| spectral_norm             | 97.3 ms                                                          | 81.6 ms: 1.19x faster                                                      |
| tomli_loads               | 2.40 sec                                                         | 2.10 sec: 1.14x faster                                                     |
| mako                      | 10.4 ms                                                          | 9.27 ms: 1.12x faster                                                      |
| create_gc_cycles          | 2.00 ms                                                          | 1.84 ms: 1.09x faster                                                      |
| richards_super            | 61.2 ms                                                          | 56.3 ms: 1.09x faster                                                      |
| richards                  | 53.4 ms                                                          | 49.3 ms: 1.08x faster                                                      |
| unpickle                  | 15.7 us                                                          | 14.6 us: 1.08x faster                                                      |
| scimark_fft               | 312 ms                                                           | 292 ms: 1.07x faster                                                       |
| sqlite_synth              | 2.80 us                                                          | 2.65 us: 1.06x faster                                                      |
| pickle_dict               | 32.8 us                                                          | 31.1 us: 1.06x faster                                                      |
| telco                     | 8.40 ms                                                          | 8.04 ms: 1.04x faster                                                      |
| async_tree_memoization    | 460 ms                                                           | 442 ms: 1.04x faster                                                       |
| float                     | 80.2 ms                                                          | 77.4 ms: 1.04x faster                                                      |
| scimark_sparse_mat_mult   | 4.28 ms                                                          | 4.14 ms: 1.03x faster                                                      |
| xml_etree_process         | 59.7 ms                                                          | 58.1 ms: 1.03x faster                                                      |
| pickle                    | 10.6 us                                                          | 10.4 us: 1.02x faster                                                      |
| xml_etree_generate        | 85.7 ms                                                          | 84.0 ms: 1.02x faster                                                      |
| html5lib                  | 74.7 ms                                                          | 73.2 ms: 1.02x faster                                                      |
| regex_dna                 | 249 ms                                                           | 245 ms: 1.02x faster                                                       |
| crypto_pyaes              | 73.6 ms                                                          | 72.3 ms: 1.02x faster                                                      |
| chameleon                 | 7.40 ms                                                          | 7.29 ms: 1.01x faster                                                      |
| asyncio_tcp               | 378 ms                                                           | 372 ms: 1.01x faster                                                       |
| async_tree_cpu_io_mixed   | 604 ms                                                           | 596 ms: 1.01x faster                                                       |
| deepcopy_reduce           | 3.39 us                                                          | 3.35 us: 1.01x faster                                                      |
| pickle_list               | 4.44 us                                                          | 4.39 us: 1.01x faster                                                      |
| genshi_xml                | 58.1 ms                                                          | 57.3 ms: 1.01x faster                                                      |
| fannkuch                  | 353 ms                                                           | 348 ms: 1.01x faster                                                       |
| coverage                  | 83.5 ms                                                          | 82.8 ms: 1.01x faster                                                      |
| thrift                    | 880 us                                                           | 873 us: 1.01x faster                                                       |
| pickle_pure_python        | 307 us                                                           | 305 us: 1.01x faster                                                       |
| pyflate                   | 482 ms                                                           | 479 ms: 1.01x faster                                                       |
| regex_v8                  | 26.0 ms                                                          | 25.9 ms: 1.00x faster                                                      |
| xml_etree_iterparse       | 103 ms                                                           | 103 ms: 1.00x slower                                                       |
| json_dumps                | 10.8 ms                                                          | 10.8 ms: 1.01x slower                                                      |
| generators                | 33.5 ms                                                          | 33.7 ms: 1.01x slower                                                      |
| gc_traversal              | 4.69 ms                                                          | 4.72 ms: 1.01x slower                                                      |
| logging_silent            | 96.3 ns                                                          | 97.2 ns: 1.01x slower                                                      |
| json                      | 5.35 ms                                                          | 5.42 ms: 1.01x slower                                                      |
| json_loads                | 25.0 us                                                          | 25.3 us: 1.01x slower                                                      |
| async_tree_io_tg          | 900 ms                                                           | 912 ms: 1.01x slower                                                       |
| regex_effbot              | 3.40 ms                                                          | 3.45 ms: 1.01x slower                                                      |
| deepcopy                  | 377 us                                                           | 383 us: 1.01x slower                                                       |
| logging_format            | 7.11 us                                                          | 7.22 us: 1.02x slower                                                      |
| regex_compile             | 144 ms                                                           | 146 ms: 1.02x slower                                                       |
| pprint_pformat            | 1.66 sec                                                         | 1.69 sec: 1.02x slower                                                     |
| deepcopy_memo             | 37.3 us                                                          | 37.9 us: 1.02x slower                                                      |
| scimark_monte_carlo       | 65.5 ms                                                          | 66.6 ms: 1.02x slower                                                      |
| pprint_safe_repr          | 818 ms                                                           | 833 ms: 1.02x slower                                                       |
| coroutines                | 22.0 ms                                                          | 22.4 ms: 1.02x slower                                                      |
| unpickle_pure_python      | 224 us                                                           | 229 us: 1.02x slower                                                       |
| django_template           | 39.0 ms                                                          | 39.8 ms: 1.02x slower                                                      |
| xml_etree_parse           | 144 ms                                                           | 147 ms: 1.02x slower                                                       |
| sympy_expand              | 501 ms                                                           | 513 ms: 1.02x slower                                                       |
| sqlglot_parse             | 1.39 ms                                                          | 1.42 ms: 1.02x slower                                                      |
| sqlglot_transpile         | 1.76 ms                                                          | 1.81 ms: 1.03x slower                                                      |
| sympy_str                 | 295 ms                                                           | 302 ms: 1.03x slower                                                       |
| 2to3                      | 291 ms                                                           | 299 ms: 1.03x slower                                                       |
| python_startup            | 13.2 ms                                                          | 13.6 ms: 1.03x slower                                                      |
| meteor_contest            | 128 ms                                                           | 132 ms: 1.03x slower                                                       |
| pidigits                  | 254 ms                                                           | 261 ms: 1.03x slower                                                       |
| dulwich_log               | 67.3 ms                                                          | 69.2 ms: 1.03x slower                                                      |
| async_tree_memoization_tg | 421 ms                                                           | 434 ms: 1.03x slower                                                       |
| logging_simple            | 6.40 us                                                          | 6.60 us: 1.03x slower                                                      |
| docutils                  | 2.98 sec                                                         | 3.08 sec: 1.03x slower                                                     |
| sqlglot_normalize         | 120 ms                                                           | 124 ms: 1.03x slower                                                       |
| genshi_text               | 25.9 ms                                                          | 26.8 ms: 1.03x slower                                                      |
| dask                      | 391 ms                                                           | 404 ms: 1.04x slower                                                       |
| go                        | 165 ms                                                           | 172 ms: 1.04x slower                                                       |
| chaos                     | 59.6 ms                                                          | 62.1 ms: 1.04x slower                                                      |
| tornado_http              | 119 ms                                                           | 124 ms: 1.04x slower                                                       |
| sympy_sum                 | 155 ms                                                           | 162 ms: 1.04x slower                                                       |
| gunicorn                  | 1.04 ms                                                          | 1.10 ms: 1.05x slower                                                      |
| aiohttp                   | 1.07 ms                                                          | 1.13 ms: 1.06x slower                                                      |
| sqlglot_optimize          | 59.5 ms                                                          | 63.1 ms: 1.06x slower                                                      |
| pycparser                 | 1.22 sec                                                         | 1.30 sec: 1.06x slower                                                     |
| async_generators          | 363 ms                                                           | 386 ms: 1.06x slower                                                       |
| mdp                       | 2.46 sec                                                         | 2.62 sec: 1.07x slower                                                     |
| mypy2                     | 764 ms                                                           | 831 ms: 1.09x slower                                                       |
| sympy_integrate           | 23.2 ms                                                          | 25.2 ms: 1.09x slower                                                      |
| deltablue                 | 3.37 ms                                                          | 3.73 ms: 1.11x slower                                                      |
| comprehensions            | 17.0 us                                                          | 18.9 us: 1.12x slower                                                      |
| hexiom                    | 6.35 ms                                                          | 7.16 ms: 1.13x slower                                                      |
| nqueens                   | 88.4 ms                                                          | 102 ms: 1.15x slower                                                       |
| pathlib                   | 17.1 ms                                                          | 19.8 ms: 1.16x slower                                                      |
| raytrace                  | 260 ms                                                           | 304 ms: 1.17x slower                                                       |
| scimark_lu                | 97.5 ms                                                          | 115 ms: 1.18x slower                                                       |
| bench_thread_pool         | 908 us                                                           | 1.11 ms: 1.23x slower                                                      |
| scimark_sor               | 119 ms                                                           | 150 ms: 1.26x slower                                                       |
| python_startup_no_site    | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                      |
| Geometric mean            | (ref)                                                            | 1.01x slower                                                               |

Benchmark hidden because not significant (10): async_tree_none, nbody, pylint, asyncio_websockets, async_tree_none_tg, unpickle_list, asyncio_tcp_ssl, async_tree_cpu_io_mixed_tg, async_tree_io, bench_mp_pool
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: unpack_sequence

# HPT report

- Reliability score: 99.86% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x