# Results vs. 3.13.0b2

- fork: python
- ref: 05e0b67a43c5c1778dc2
- machine: windows-amd64
- commit hash: 05e0b67
- commit date: 2024-03-29
- overall geometric mean: 1.01x slower
- HPT reliability: 99.72%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 218 ms: 1.05x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.85 ms: 1.01x slower                                                       |
| docutils       | 1.63 sec                                                        | 1.68 sec: 1.03x slower                                                      |
| html5lib       | 35.0 ms                                                         | 35.2 ms: 1.00x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 84.1 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|-------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 389 ms                                                          | 375 ms: 1.04x faster                                                        |
| Geometric mean          | (ref)                                                           | 1.01x faster                                                                |

Benchmark hidden because not significant (7): async_tree_io, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 58.4 ms: 1.16x faster                                                       |
| float          | 49.7 ms                                                         | 46.4 ms: 1.07x faster                                                       |
| pidigits       | 150 ms                                                          | 146 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                          | 120 ms: 1.01x slower                                                        |
| regex_effbot   | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                       |
| regex_compile  | 78.0 ms                                                         | 81.4 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.18 sec: 1.14x faster                                                      |
| json_loads           | 14.2 us                                                         | 13.7 us: 1.03x faster                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 60.4 ms: 1.03x faster                                                       |
| json_dumps           | 5.61 ms                                                         | 5.47 ms: 1.03x faster                                                       |
| xml_etree_process    | 36.4 ms                                                         | 35.8 ms: 1.02x faster                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 52.3 ms: 1.02x faster                                                       |
| xml_etree_parse      | 90.9 ms                                                         | 89.5 ms: 1.02x faster                                                       |
| pickle_pure_python   | 175 us                                                          | 174 us: 1.01x faster                                                        |
| pickle_dict          | 18.1 us                                                         | 18.6 us: 1.03x slower                                                       |
| unpickle             | 8.40 us                                                         | 8.71 us: 1.04x slower                                                       |
| pickle               | 7.11 us                                                         | 7.54 us: 1.06x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.79 us: 1.07x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 133 us: 1.09x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.00x faster                                                                |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 21.6 ms: 1.07x slower                                                       |
| python_startup_no_site | 16.2 ms                                                         | 19.4 ms: 1.20x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 5.70 ms: 1.12x faster                                                       |
| django_template | 21.7 ms                                                         | 22.0 ms: 1.01x slower                                                       |
| genshi_xml      | 31.6 ms                                                         | 33.6 ms: 1.06x slower                                                       |
| genshi_text     | 14.4 ms                                                         | 15.3 ms: 1.06x slower                                                       |
| Geometric mean  | (ref)                                                           | 1.01x slower                                                                |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 70.1 us: 1.44x faster                                                       |
| spectral_norm            | 63.7 ms                                                         | 50.9 ms: 1.25x faster                                                       |
| nbody                    | 67.6 ms                                                         | 58.4 ms: 1.16x faster                                                       |
| tomli_loads              | 1.35 sec                                                        | 1.18 sec: 1.14x faster                                                      |
| mako                     | 6.36 ms                                                         | 5.70 ms: 1.12x faster                                                       |
| pycparser                | 754 ms                                                          | 677 ms: 1.11x faster                                                        |
| fannkuch                 | 243 ms                                                          | 224 ms: 1.09x faster                                                        |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.30 ms: 1.09x faster                                                       |
| float                    | 49.7 ms                                                         | 46.4 ms: 1.07x faster                                                       |
| pylint                   | 205 ms                                                          | 194 ms: 1.05x faster                                                        |
| create_gc_cycles         | 888 us                                                          | 855 us: 1.04x faster                                                        |
| deepcopy_reduce          | 1.99 us                                                         | 1.92 us: 1.04x faster                                                       |
| async_tree_cpu_io_mixed  | 389 ms                                                          | 375 ms: 1.04x faster                                                        |
| json_loads               | 14.2 us                                                         | 13.7 us: 1.03x faster                                                       |
| xml_etree_iterparse      | 62.3 ms                                                         | 60.4 ms: 1.03x faster                                                       |
| crypto_pyaes             | 45.5 ms                                                         | 44.1 ms: 1.03x faster                                                       |
| json_dumps               | 5.61 ms                                                         | 5.47 ms: 1.03x faster                                                       |
| pidigits                 | 150 ms                                                          | 146 ms: 1.02x faster                                                        |
| deepcopy_memo            | 22.1 us                                                         | 21.7 us: 1.02x faster                                                       |
| xml_etree_process        | 36.4 ms                                                         | 35.8 ms: 1.02x faster                                                       |
| xml_etree_generate       | 53.2 ms                                                         | 52.3 ms: 1.02x faster                                                       |
| pprint_safe_repr         | 474 ms                                                          | 467 ms: 1.02x faster                                                        |
| xml_etree_parse          | 90.9 ms                                                         | 89.5 ms: 1.02x faster                                                       |
| gc_traversal             | 1.55 ms                                                         | 1.53 ms: 1.01x faster                                                       |
| pickle_pure_python       | 175 us                                                          | 174 us: 1.01x faster                                                        |
| sqlite_synth             | 1.60 us                                                         | 1.58 us: 1.01x faster                                                       |
| deepcopy                 | 220 us                                                          | 218 us: 1.01x faster                                                        |
| pprint_pformat           | 966 ms                                                          | 962 ms: 1.00x faster                                                        |
| telco                    | 4.67 ms                                                         | 4.69 ms: 1.00x slower                                                       |
| html5lib                 | 35.0 ms                                                         | 35.2 ms: 1.00x slower                                                       |
| regex_dna                | 119 ms                                                          | 120 ms: 1.01x slower                                                        |
| logging_simple           | 5.78 us                                                         | 5.83 us: 1.01x slower                                                       |
| chameleon                | 4.80 ms                                                         | 4.85 ms: 1.01x slower                                                       |
| aiohttp                  | 889 us                                                          | 896 us: 1.01x slower                                                        |
| regex_effbot             | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                       |
| generators               | 19.6 ms                                                         | 19.8 ms: 1.01x slower                                                       |
| django_template          | 21.7 ms                                                         | 22.0 ms: 1.01x slower                                                       |
| coroutines               | 12.8 ms                                                         | 13.0 ms: 1.02x slower                                                       |
| sqlglot_parse            | 748 us                                                          | 764 us: 1.02x slower                                                        |
| pathlib                  | 75.9 ms                                                         | 77.5 ms: 1.02x slower                                                       |
| sympy_sum                | 84.4 ms                                                         | 86.2 ms: 1.02x slower                                                       |
| pyflate                  | 279 ms                                                          | 286 ms: 1.03x slower                                                        |
| pickle_dict              | 18.1 us                                                         | 18.6 us: 1.03x slower                                                       |
| tornado_http             | 81.8 ms                                                         | 84.1 ms: 1.03x slower                                                       |
| docutils                 | 1.63 sec                                                        | 1.68 sec: 1.03x slower                                                      |
| sympy_str                | 159 ms                                                          | 164 ms: 1.03x slower                                                        |
| sqlglot_transpile        | 955 us                                                          | 986 us: 1.03x slower                                                        |
| unpickle                 | 8.40 us                                                         | 8.71 us: 1.04x slower                                                       |
| sympy_expand             | 271 ms                                                          | 281 ms: 1.04x slower                                                        |
| bench_mp_pool            | 64.8 ms                                                         | 67.3 ms: 1.04x slower                                                       |
| regex_compile            | 78.0 ms                                                         | 81.4 ms: 1.04x slower                                                       |
| meteor_contest           | 69.9 ms                                                         | 73.1 ms: 1.05x slower                                                       |
| mdp                      | 1.31 sec                                                        | 1.38 sec: 1.05x slower                                                      |
| 2to3                     | 207 ms                                                          | 218 ms: 1.05x slower                                                        |
| deltablue                | 1.88 ms                                                         | 1.98 ms: 1.05x slower                                                       |
| sqlglot_normalize        | 173 ms                                                          | 182 ms: 1.05x slower                                                        |
| richards_super           | 30.2 ms                                                         | 31.9 ms: 1.06x slower                                                       |
| pickle                   | 7.11 us                                                         | 7.54 us: 1.06x slower                                                       |
| comprehensions           | 10.4 us                                                         | 11.0 us: 1.06x slower                                                       |
| dulwich_log              | 38.0 ms                                                         | 40.4 ms: 1.06x slower                                                       |
| bench_thread_pool        | 768 us                                                          | 816 us: 1.06x slower                                                        |
| genshi_xml               | 31.6 ms                                                         | 33.6 ms: 1.06x slower                                                       |
| genshi_text              | 14.4 ms                                                         | 15.3 ms: 1.06x slower                                                       |
| python_startup           | 20.3 ms                                                         | 21.6 ms: 1.07x slower                                                       |
| unpickle_list            | 2.62 us                                                         | 2.79 us: 1.07x slower                                                       |
| sympy_integrate          | 12.2 ms                                                         | 13.0 ms: 1.07x slower                                                       |
| mypy2                    | 418 ms                                                          | 446 ms: 1.07x slower                                                        |
| async_generators         | 223 ms                                                          | 238 ms: 1.07x slower                                                        |
| sqlglot_optimize         | 32.7 ms                                                         | 35.0 ms: 1.07x slower                                                       |
| richards                 | 26.7 ms                                                         | 28.6 ms: 1.07x slower                                                       |
| scimark_sor              | 75.3 ms                                                         | 80.8 ms: 1.07x slower                                                       |
| nqueens                  | 56.7 ms                                                         | 61.0 ms: 1.08x slower                                                       |
| unpickle_pure_python     | 122 us                                                          | 133 us: 1.09x slower                                                        |
| coverage                 | 42.1 ms                                                         | 46.2 ms: 1.10x slower                                                       |
| raytrace                 | 162 ms                                                          | 178 ms: 1.10x slower                                                        |
| thrift                   | 8.11 ms                                                         | 9.00 ms: 1.11x slower                                                       |
| go                       | 82.1 ms                                                         | 93.0 ms: 1.13x slower                                                       |
| json                     | 3.19 ms                                                         | 3.75 ms: 1.18x slower                                                       |
| python_startup_no_site   | 16.2 ms                                                         | 19.4 ms: 1.20x slower                                                       |
| hexiom                   | 3.72 ms                                                         | 4.52 ms: 1.21x slower                                                       |
| scimark_lu               | 56.6 ms                                                         | 74.4 ms: 1.31x slower                                                       |
| Geometric mean           | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (16): async_tree_io, async_tree_none, asyncio_tcp_ssl, scimark_fft, logging_format, scimark_monte_carlo, async_tree_cpu_io_mixed_tg, async_tree_none_tg, logging_silent, asyncio_tcp, chaos, pickle_list, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, regex_v8
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-05e0b67-JIT/bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67.json: unpack_sequence

# HPT report

- Reliability score: 99.72% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown