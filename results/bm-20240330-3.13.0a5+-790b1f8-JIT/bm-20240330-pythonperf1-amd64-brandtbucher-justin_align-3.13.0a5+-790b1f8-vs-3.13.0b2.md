# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_align
- machine: windows-amd64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 220 ms: 1.06x slower                                                      |
| chameleon      | 4.80 ms                                                         | 4.74 ms: 1.01x faster                                                     |
| docutils       | 1.63 sec                                                        | 1.69 sec: 1.04x slower                                                    |
| html5lib       | 35.0 ms                                                         | 36.5 ms: 1.04x slower                                                     |
| tornado_http   | 81.8 ms                                                         | 83.9 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                           | 1.03x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 389 ms                                                          | 375 ms: 1.04x faster                                                      |
| async_tree_io           | 588 ms                                                          | 570 ms: 1.03x faster                                                      |
| Geometric mean          | (ref)                                                           | 1.00x faster                                                              |

Benchmark hidden because not significant (6): async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 59.0 ms: 1.15x faster                                                     |
| float          | 49.7 ms                                                         | 47.2 ms: 1.05x faster                                                     |
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                           | 1.07x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.2 ms: 1.11x faster                                                     |
| regex_effbot   | 1.58 ms                                                         | 1.56 ms: 1.02x faster                                                     |
| regex_dna      | 119 ms                                                          | 118 ms: 1.01x faster                                                      |
| regex_compile  | 78.0 ms                                                         | 89.1 ms: 1.14x slower                                                     |
| Geometric mean | (ref)                                                           | 1.00x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.32 sec: 1.02x faster                                                    |
| pickle_pure_python   | 175 us                                                          | 172 us: 1.02x faster                                                      |
| xml_etree_iterparse  | 62.3 ms                                                         | 61.3 ms: 1.02x faster                                                     |
| xml_etree_parse      | 90.9 ms                                                         | 89.6 ms: 1.01x faster                                                     |
| json_dumps           | 5.61 ms                                                         | 5.57 ms: 1.01x faster                                                     |
| xml_etree_generate   | 53.2 ms                                                         | 53.0 ms: 1.00x faster                                                     |
| pickle               | 7.11 us                                                         | 7.16 us: 1.01x slower                                                     |
| xml_etree_process    | 36.4 ms                                                         | 37.0 ms: 1.02x slower                                                     |
| pickle_dict          | 18.1 us                                                         | 18.5 us: 1.02x slower                                                     |
| unpickle             | 8.40 us                                                         | 8.56 us: 1.02x slower                                                     |
| json_loads           | 14.2 us                                                         | 14.5 us: 1.03x slower                                                     |
| unpickle_list        | 2.62 us                                                         | 2.74 us: 1.04x slower                                                     |
| unpickle_pure_python | 122 us                                                          | 136 us: 1.12x slower                                                      |
| Geometric mean       | (ref)                                                           | 1.01x slower                                                              |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 21.9 ms: 1.08x slower                                                     |
| python_startup_no_site | 16.2 ms                                                         | 19.6 ms: 1.21x slower                                                     |
| Geometric mean         | (ref)                                                           | 1.14x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 6.08 ms: 1.05x faster                                                     |
| django_template | 21.7 ms                                                         | 22.5 ms: 1.04x slower                                                     |
| genshi_text     | 14.4 ms                                                         | 15.0 ms: 1.04x slower                                                     |
| genshi_xml      | 31.6 ms                                                         | 33.3 ms: 1.05x slower                                                     |
| Geometric mean  | (ref)                                                           | 1.02x slower                                                              |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 70.6 us: 1.43x faster                                                     |
| spectral_norm            | 63.7 ms                                                         | 55.6 ms: 1.15x faster                                                     |
| nbody                    | 67.6 ms                                                         | 59.0 ms: 1.15x faster                                                     |
| regex_v8                 | 15.8 ms                                                         | 14.2 ms: 1.11x faster                                                     |
| float                    | 49.7 ms                                                         | 47.2 ms: 1.05x faster                                                     |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.38 ms: 1.05x faster                                                     |
| pylint                   | 205 ms                                                          | 195 ms: 1.05x faster                                                      |
| mako                     | 6.36 ms                                                         | 6.08 ms: 1.05x faster                                                     |
| create_gc_cycles         | 888 us                                                          | 851 us: 1.04x faster                                                      |
| async_tree_cpu_io_mixed  | 389 ms                                                          | 375 ms: 1.04x faster                                                      |
| async_tree_io            | 588 ms                                                          | 570 ms: 1.03x faster                                                      |
| deepcopy_reduce          | 1.99 us                                                         | 1.94 us: 1.03x faster                                                     |
| tomli_loads              | 1.35 sec                                                        | 1.32 sec: 1.02x faster                                                    |
| gc_traversal             | 1.55 ms                                                         | 1.52 ms: 1.02x faster                                                     |
| pickle_pure_python       | 175 us                                                          | 172 us: 1.02x faster                                                      |
| regex_effbot             | 1.58 ms                                                         | 1.56 ms: 1.02x faster                                                     |
| pidigits                 | 150 ms                                                          | 147 ms: 1.02x faster                                                      |
| xml_etree_iterparse      | 62.3 ms                                                         | 61.3 ms: 1.02x faster                                                     |
| xml_etree_parse          | 90.9 ms                                                         | 89.6 ms: 1.01x faster                                                     |
| chameleon                | 4.80 ms                                                         | 4.74 ms: 1.01x faster                                                     |
| crypto_pyaes             | 45.5 ms                                                         | 44.9 ms: 1.01x faster                                                     |
| regex_dna                | 119 ms                                                          | 118 ms: 1.01x faster                                                      |
| json_dumps               | 5.61 ms                                                         | 5.57 ms: 1.01x faster                                                     |
| xml_etree_generate       | 53.2 ms                                                         | 53.0 ms: 1.00x faster                                                     |
| pickle                   | 7.11 us                                                         | 7.16 us: 1.01x slower                                                     |
| deepcopy_memo            | 22.1 us                                                         | 22.3 us: 1.01x slower                                                     |
| xml_etree_process        | 36.4 ms                                                         | 37.0 ms: 1.02x slower                                                     |
| aiohttp                  | 889 us                                                          | 903 us: 1.02x slower                                                      |
| pickle_dict              | 18.1 us                                                         | 18.5 us: 1.02x slower                                                     |
| unpickle                 | 8.40 us                                                         | 8.56 us: 1.02x slower                                                     |
| pathlib                  | 75.9 ms                                                         | 77.5 ms: 1.02x slower                                                     |
| json_loads               | 14.2 us                                                         | 14.5 us: 1.03x slower                                                     |
| tornado_http             | 81.8 ms                                                         | 83.9 ms: 1.03x slower                                                     |
| coroutines               | 12.8 ms                                                         | 13.1 ms: 1.03x slower                                                     |
| bench_mp_pool            | 64.8 ms                                                         | 67.3 ms: 1.04x slower                                                     |
| docutils                 | 1.63 sec                                                        | 1.69 sec: 1.04x slower                                                    |
| django_template          | 21.7 ms                                                         | 22.5 ms: 1.04x slower                                                     |
| generators               | 19.6 ms                                                         | 20.3 ms: 1.04x slower                                                     |
| scimark_fft              | 171 ms                                                          | 178 ms: 1.04x slower                                                      |
| sympy_sum                | 84.4 ms                                                         | 87.9 ms: 1.04x slower                                                     |
| html5lib                 | 35.0 ms                                                         | 36.5 ms: 1.04x slower                                                     |
| genshi_text              | 14.4 ms                                                         | 15.0 ms: 1.04x slower                                                     |
| unpickle_list            | 2.62 us                                                         | 2.74 us: 1.04x slower                                                     |
| chaos                    | 38.4 ms                                                         | 40.1 ms: 1.05x slower                                                     |
| logging_format           | 6.22 us                                                         | 6.51 us: 1.05x slower                                                     |
| pprint_safe_repr         | 474 ms                                                          | 496 ms: 1.05x slower                                                      |
| logging_simple           | 5.78 us                                                         | 6.05 us: 1.05x slower                                                     |
| meteor_contest           | 69.9 ms                                                         | 73.4 ms: 1.05x slower                                                     |
| telco                    | 4.67 ms                                                         | 4.91 ms: 1.05x slower                                                     |
| sqlglot_normalize        | 173 ms                                                          | 182 ms: 1.05x slower                                                      |
| genshi_xml               | 31.6 ms                                                         | 33.3 ms: 1.05x slower                                                     |
| sympy_str                | 159 ms                                                          | 168 ms: 1.06x slower                                                      |
| sqlglot_transpile        | 955 us                                                          | 1.01 ms: 1.06x slower                                                     |
| coverage                 | 42.1 ms                                                         | 44.7 ms: 1.06x slower                                                     |
| pyflate                  | 279 ms                                                          | 296 ms: 1.06x slower                                                      |
| 2to3                     | 207 ms                                                          | 220 ms: 1.06x slower                                                      |
| sqlglot_parse            | 748 us                                                          | 796 us: 1.06x slower                                                      |
| sympy_expand             | 271 ms                                                          | 290 ms: 1.07x slower                                                      |
| pprint_pformat           | 966 ms                                                          | 1.03 sec: 1.07x slower                                                    |
| deltablue                | 1.88 ms                                                         | 2.02 ms: 1.07x slower                                                     |
| dulwich_log              | 38.0 ms                                                         | 40.9 ms: 1.07x slower                                                     |
| bench_thread_pool        | 768 us                                                          | 828 us: 1.08x slower                                                      |
| sqlglot_optimize         | 32.7 ms                                                         | 35.3 ms: 1.08x slower                                                     |
| fannkuch                 | 243 ms                                                          | 263 ms: 1.08x slower                                                      |
| scimark_monte_carlo      | 39.1 ms                                                         | 42.3 ms: 1.08x slower                                                     |
| python_startup           | 20.3 ms                                                         | 21.9 ms: 1.08x slower                                                     |
| mypy2                    | 418 ms                                                          | 453 ms: 1.08x slower                                                      |
| async_generators         | 223 ms                                                          | 244 ms: 1.09x slower                                                      |
| sympy_integrate          | 12.2 ms                                                         | 13.4 ms: 1.09x slower                                                     |
| raytrace                 | 162 ms                                                          | 178 ms: 1.10x slower                                                      |
| asyncio_tcp_ssl          | 1.48 sec                                                        | 1.63 sec: 1.10x slower                                                    |
| scimark_sor              | 75.3 ms                                                         | 84.1 ms: 1.12x slower                                                     |
| unpickle_pure_python     | 122 us                                                          | 136 us: 1.12x slower                                                      |
| nqueens                  | 56.7 ms                                                         | 63.6 ms: 1.12x slower                                                     |
| richards_super           | 30.2 ms                                                         | 34.4 ms: 1.14x slower                                                     |
| regex_compile            | 78.0 ms                                                         | 89.1 ms: 1.14x slower                                                     |
| thrift                   | 8.11 ms                                                         | 9.29 ms: 1.15x slower                                                     |
| comprehensions           | 10.4 us                                                         | 12.0 us: 1.15x slower                                                     |
| richards                 | 26.7 ms                                                         | 31.0 ms: 1.16x slower                                                     |
| mdp                      | 1.31 sec                                                        | 1.54 sec: 1.17x slower                                                    |
| go                       | 82.1 ms                                                         | 96.7 ms: 1.18x slower                                                     |
| python_startup_no_site   | 16.2 ms                                                         | 19.6 ms: 1.21x slower                                                     |
| scimark_lu               | 56.6 ms                                                         | 75.5 ms: 1.33x slower                                                     |
| hexiom                   | 3.72 ms                                                         | 5.22 ms: 1.40x slower                                                     |
| Geometric mean           | (ref)                                                           | 1.03x slower                                                              |

Benchmark hidden because not significant (13): pycparser, async_tree_none, pickle_list, async_tree_cpu_io_mixed_tg, deepcopy, sqlite_synth, json, async_tree_none_tg, logging_silent, async_tree_io_tg, async_tree_memoization, asyncio_tcp, async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: unknown