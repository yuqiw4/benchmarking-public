# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_align
- machine: windows-amd64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.01x slower
- HPT reliability: 99.55%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 217 ms: 1.05x slower                                                      |
| chameleon      | 4.80 ms                                                         | 4.86 ms: 1.01x slower                                                     |
| docutils       | 1.63 sec                                                        | 1.68 sec: 1.03x slower                                                    |
| html5lib       | 35.0 ms                                                         | 35.5 ms: 1.01x slower                                                     |
| tornado_http   | 81.8 ms                                                         | 83.5 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                           | 1.03x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io           | 588 ms                                                          | 565 ms: 1.04x faster                                                      |
| async_tree_cpu_io_mixed | 389 ms                                                          | 376 ms: 1.03x faster                                                      |
| async_tree_none         | 218 ms                                                          | 213 ms: 1.02x faster                                                      |
| Geometric mean          | (ref)                                                           | 1.01x faster                                                              |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 57.7 ms: 1.17x faster                                                     |
| float          | 49.7 ms                                                         | 47.3 ms: 1.05x faster                                                     |
| pidigits       | 150 ms                                                          | 146 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                           | 1.08x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.7 ms: 1.07x faster                                                     |
| regex_effbot   | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                     |
| regex_dna      | 119 ms                                                          | 119 ms: 1.00x slower                                                      |
| regex_compile  | 78.0 ms                                                         | 83.3 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                           | 1.00x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.20 sec: 1.12x faster                                                    |
| json_dumps           | 5.61 ms                                                         | 5.51 ms: 1.02x faster                                                     |
| xml_etree_iterparse  | 62.3 ms                                                         | 61.4 ms: 1.01x faster                                                     |
| pickle_pure_python   | 175 us                                                          | 174 us: 1.01x faster                                                      |
| pickle_dict          | 18.1 us                                                         | 18.3 us: 1.01x slower                                                     |
| json_loads           | 14.2 us                                                         | 14.4 us: 1.02x slower                                                     |
| pickle               | 7.11 us                                                         | 7.37 us: 1.04x slower                                                     |
| unpickle             | 8.40 us                                                         | 8.70 us: 1.04x slower                                                     |
| unpickle_list        | 2.62 us                                                         | 2.74 us: 1.05x slower                                                     |
| unpickle_pure_python | 122 us                                                          | 129 us: 1.06x slower                                                      |
| Geometric mean       | (ref)                                                           | 1.00x slower                                                              |

Benchmark hidden because not significant (4): xml_etree_process, xml_etree_generate, pickle_list, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 22.3 ms: 1.10x slower                                                     |
| python_startup_no_site | 16.2 ms                                                         | 20.3 ms: 1.25x slower                                                     |
| Geometric mean         | (ref)                                                           | 1.17x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 5.75 ms: 1.11x faster                                                     |
| django_template | 21.7 ms                                                         | 22.5 ms: 1.04x slower                                                     |
| genshi_text     | 14.4 ms                                                         | 15.0 ms: 1.04x slower                                                     |
| genshi_xml      | 31.6 ms                                                         | 33.0 ms: 1.04x slower                                                     |
| Geometric mean  | (ref)                                                           | 1.01x slower                                                              |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 69.0 us: 1.46x faster                                                     |
| spectral_norm            | 63.7 ms                                                         | 51.1 ms: 1.25x faster                                                     |
| nbody                    | 67.6 ms                                                         | 57.7 ms: 1.17x faster                                                     |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.22 ms: 1.13x faster                                                     |
| tomli_loads              | 1.35 sec                                                        | 1.20 sec: 1.12x faster                                                    |
| mako                     | 6.36 ms                                                         | 5.75 ms: 1.11x faster                                                     |
| json                     | 3.19 ms                                                         | 2.97 ms: 1.07x faster                                                     |
| regex_v8                 | 15.8 ms                                                         | 14.7 ms: 1.07x faster                                                     |
| fannkuch                 | 243 ms                                                          | 229 ms: 1.06x faster                                                      |
| float                    | 49.7 ms                                                         | 47.3 ms: 1.05x faster                                                     |
| deepcopy_reduce          | 1.99 us                                                         | 1.90 us: 1.05x faster                                                     |
| pylint                   | 205 ms                                                          | 195 ms: 1.05x faster                                                      |
| async_tree_io            | 588 ms                                                          | 565 ms: 1.04x faster                                                      |
| create_gc_cycles         | 888 us                                                          | 855 us: 1.04x faster                                                      |
| deepcopy_memo            | 22.1 us                                                         | 21.3 us: 1.04x faster                                                     |
| async_tree_cpu_io_mixed  | 389 ms                                                          | 376 ms: 1.03x faster                                                      |
| crypto_pyaes             | 45.5 ms                                                         | 44.0 ms: 1.03x faster                                                     |
| pidigits                 | 150 ms                                                          | 146 ms: 1.02x faster                                                      |
| async_tree_none          | 218 ms                                                          | 213 ms: 1.02x faster                                                      |
| json_dumps               | 5.61 ms                                                         | 5.51 ms: 1.02x faster                                                     |
| gc_traversal             | 1.55 ms                                                         | 1.53 ms: 1.02x faster                                                     |
| xml_etree_iterparse      | 62.3 ms                                                         | 61.4 ms: 1.01x faster                                                     |
| pprint_safe_repr         | 474 ms                                                          | 467 ms: 1.01x faster                                                      |
| pprint_pformat           | 966 ms                                                          | 953 ms: 1.01x faster                                                      |
| deepcopy                 | 220 us                                                          | 217 us: 1.01x faster                                                      |
| generators               | 19.6 ms                                                         | 19.3 ms: 1.01x faster                                                     |
| regex_effbot             | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                     |
| scimark_fft              | 171 ms                                                          | 170 ms: 1.01x faster                                                      |
| pickle_pure_python       | 175 us                                                          | 174 us: 1.01x faster                                                      |
| telco                    | 4.67 ms                                                         | 4.65 ms: 1.00x faster                                                     |
| regex_dna                | 119 ms                                                          | 119 ms: 1.00x slower                                                      |
| pickle_dict              | 18.1 us                                                         | 18.3 us: 1.01x slower                                                     |
| chameleon                | 4.80 ms                                                         | 4.86 ms: 1.01x slower                                                     |
| aiohttp                  | 889 us                                                          | 899 us: 1.01x slower                                                      |
| html5lib                 | 35.0 ms                                                         | 35.5 ms: 1.01x slower                                                     |
| json_loads               | 14.2 us                                                         | 14.4 us: 1.02x slower                                                     |
| chaos                    | 38.4 ms                                                         | 39.0 ms: 1.02x slower                                                     |
| pathlib                  | 75.9 ms                                                         | 77.4 ms: 1.02x slower                                                     |
| tornado_http             | 81.8 ms                                                         | 83.5 ms: 1.02x slower                                                     |
| scimark_monte_carlo      | 39.1 ms                                                         | 40.3 ms: 1.03x slower                                                     |
| sqlglot_parse            | 748 us                                                          | 772 us: 1.03x slower                                                      |
| docutils                 | 1.63 sec                                                        | 1.68 sec: 1.03x slower                                                    |
| meteor_contest           | 69.9 ms                                                         | 72.3 ms: 1.03x slower                                                     |
| pickle                   | 7.11 us                                                         | 7.37 us: 1.04x slower                                                     |
| unpickle                 | 8.40 us                                                         | 8.70 us: 1.04x slower                                                     |
| django_template          | 21.7 ms                                                         | 22.5 ms: 1.04x slower                                                     |
| sqlglot_transpile        | 955 us                                                          | 990 us: 1.04x slower                                                      |
| bench_mp_pool            | 64.8 ms                                                         | 67.3 ms: 1.04x slower                                                     |
| sympy_str                | 159 ms                                                          | 166 ms: 1.04x slower                                                      |
| sympy_sum                | 84.4 ms                                                         | 88.1 ms: 1.04x slower                                                     |
| genshi_text              | 14.4 ms                                                         | 15.0 ms: 1.04x slower                                                     |
| genshi_xml               | 31.6 ms                                                         | 33.0 ms: 1.04x slower                                                     |
| sqlglot_normalize        | 173 ms                                                          | 181 ms: 1.04x slower                                                      |
| unpickle_list            | 2.62 us                                                         | 2.74 us: 1.05x slower                                                     |
| 2to3                     | 207 ms                                                          | 217 ms: 1.05x slower                                                      |
| sympy_expand             | 271 ms                                                          | 284 ms: 1.05x slower                                                      |
| mdp                      | 1.31 sec                                                        | 1.38 sec: 1.05x slower                                                    |
| nqueens                  | 56.7 ms                                                         | 59.8 ms: 1.06x slower                                                     |
| unpickle_pure_python     | 122 us                                                          | 129 us: 1.06x slower                                                      |
| sqlglot_optimize         | 32.7 ms                                                         | 34.9 ms: 1.07x slower                                                     |
| mypy2                    | 418 ms                                                          | 446 ms: 1.07x slower                                                      |
| regex_compile            | 78.0 ms                                                         | 83.3 ms: 1.07x slower                                                     |
| richards_super           | 30.2 ms                                                         | 32.2 ms: 1.07x slower                                                     |
| deltablue                | 1.88 ms                                                         | 2.02 ms: 1.07x slower                                                     |
| bench_thread_pool        | 768 us                                                          | 824 us: 1.07x slower                                                      |
| richards                 | 26.7 ms                                                         | 28.7 ms: 1.07x slower                                                     |
| async_generators         | 223 ms                                                          | 241 ms: 1.08x slower                                                      |
| sympy_integrate          | 12.2 ms                                                         | 13.2 ms: 1.08x slower                                                     |
| raytrace                 | 162 ms                                                          | 176 ms: 1.08x slower                                                      |
| dulwich_log              | 38.0 ms                                                         | 41.2 ms: 1.08x slower                                                     |
| comprehensions           | 10.4 us                                                         | 11.3 us: 1.09x slower                                                     |
| thrift                   | 8.11 ms                                                         | 8.83 ms: 1.09x slower                                                     |
| python_startup           | 20.3 ms                                                         | 22.3 ms: 1.10x slower                                                     |
| coverage                 | 42.1 ms                                                         | 46.6 ms: 1.11x slower                                                     |
| scimark_sor              | 75.3 ms                                                         | 83.8 ms: 1.11x slower                                                     |
| go                       | 82.1 ms                                                         | 92.2 ms: 1.12x slower                                                     |
| hexiom                   | 3.72 ms                                                         | 4.53 ms: 1.22x slower                                                     |
| python_startup_no_site   | 16.2 ms                                                         | 20.3 ms: 1.25x slower                                                     |
| scimark_lu               | 56.6 ms                                                         | 79.9 ms: 1.41x slower                                                     |
| Geometric mean           | (ref)                                                           | 1.01x slower                                                              |

Benchmark hidden because not significant (18): pycparser, asyncio_tcp, pyflate, xml_etree_process, logging_silent, async_tree_none_tg, sqlite_synth, xml_etree_generate, logging_format, pickle_list, async_tree_memoization, logging_simple, async_tree_cpu_io_mixed_tg, coroutines, xml_etree_parse, async_tree_io_tg, async_tree_memoization_tg, asyncio_tcp_ssl
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-d1a7b3a-JIT/bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a.json: unpack_sequence

# HPT report

- Reliability score: 99.55% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown