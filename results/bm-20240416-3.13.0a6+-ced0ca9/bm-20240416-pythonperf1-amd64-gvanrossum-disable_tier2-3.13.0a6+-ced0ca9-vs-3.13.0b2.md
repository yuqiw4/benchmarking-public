# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: ced0ca9
- commit date: 2024-04-16
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 210 ms: 1.01x slower                                                     |
| docutils       | 1.63 sec                                                        | 1.65 sec: 1.01x slower                                                   |
| html5lib       | 35.0 ms                                                         | 35.8 ms: 1.02x slower                                                    |
| tornado_http   | 81.8 ms                                                         | 80.8 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                           | 1.01x slower                                                             |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|--------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg   | 605 ms                                                          | 617 ms: 1.02x slower                                                     |
| async_tree_none    | 218 ms                                                          | 222 ms: 1.02x slower                                                     |
| async_tree_none_tg | 202 ms                                                          | 217 ms: 1.08x slower                                                     |
| Geometric mean     | (ref)                                                           | 1.02x slower                                                             |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                     |
| float          | 49.7 ms                                                         | 50.7 ms: 1.02x slower                                                    |
| nbody          | 67.6 ms                                                         | 70.8 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                           | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                          | 116 ms: 1.02x faster                                                     |
| regex_effbot   | 1.58 ms                                                         | 1.55 ms: 1.02x faster                                                    |
| regex_compile  | 78.0 ms                                                         | 79.8 ms: 1.02x slower                                                    |
| regex_v8       | 15.8 ms                                                         | 18.3 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                           | 1.03x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.9 us: 1.02x faster                                                    |
| unpickle             | 8.40 us                                                         | 8.25 us: 1.02x faster                                                    |
| json_dumps           | 5.61 ms                                                         | 5.64 ms: 1.01x slower                                                    |
| xml_etree_process    | 36.4 ms                                                         | 37.2 ms: 1.02x slower                                                    |
| xml_etree_parse      | 90.9 ms                                                         | 92.8 ms: 1.02x slower                                                    |
| xml_etree_generate   | 53.2 ms                                                         | 54.5 ms: 1.02x slower                                                    |
| pickle_dict          | 18.1 us                                                         | 18.6 us: 1.03x slower                                                    |
| xml_etree_iterparse  | 62.3 ms                                                         | 64.1 ms: 1.03x slower                                                    |
| unpickle_pure_python | 122 us                                                          | 125 us: 1.03x slower                                                     |
| tomli_loads          | 1.35 sec                                                        | 1.41 sec: 1.05x slower                                                   |
| unpickle_list        | 2.62 us                                                         | 2.83 us: 1.08x slower                                                    |
| pickle_list          | 2.90 us                                                         | 3.16 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                           | 1.02x slower                                                             |

Benchmark hidden because not significant (2): pickle, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 19.7 ms: 1.03x faster                                                    |
| python_startup_no_site | 16.2 ms                                                         | 16.0 ms: 1.02x faster                                                    |
| Geometric mean         | (ref)                                                           | 1.02x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 21.7 ms                                                         | 22.5 ms: 1.04x slower                                                    |
| genshi_xml      | 31.6 ms                                                         | 33.5 ms: 1.06x slower                                                    |
| genshi_text     | 14.4 ms                                                         | 15.9 ms: 1.11x slower                                                    |
| Geometric mean  | (ref)                                                           | 1.05x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-ced0ca9 |
|--------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 73.9 us: 1.37x faster                                                    |
| pycparser                | 754 ms                                                          | 689 ms: 1.09x faster                                                     |
| raytrace                 | 162 ms                                                          | 156 ms: 1.04x faster                                                     |
| python_startup           | 20.3 ms                                                         | 19.7 ms: 1.03x faster                                                    |
| thrift                   | 8.11 ms                                                         | 7.91 ms: 1.02x faster                                                    |
| json_loads               | 14.2 us                                                         | 13.9 us: 1.02x faster                                                    |
| regex_dna                | 119 ms                                                          | 116 ms: 1.02x faster                                                     |
| regex_effbot             | 1.58 ms                                                         | 1.55 ms: 1.02x faster                                                    |
| spectral_norm            | 63.7 ms                                                         | 62.5 ms: 1.02x faster                                                    |
| pidigits                 | 150 ms                                                          | 147 ms: 1.02x faster                                                     |
| unpickle                 | 8.40 us                                                         | 8.25 us: 1.02x faster                                                    |
| aiohttp                  | 889 us                                                          | 875 us: 1.02x faster                                                     |
| python_startup_no_site   | 16.2 ms                                                         | 16.0 ms: 1.02x faster                                                    |
| bench_mp_pool            | 64.8 ms                                                         | 63.8 ms: 1.01x faster                                                    |
| tornado_http             | 81.8 ms                                                         | 80.8 ms: 1.01x faster                                                    |
| deepcopy_memo            | 22.1 us                                                         | 21.8 us: 1.01x faster                                                    |
| gc_traversal             | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                    |
| richards                 | 26.7 ms                                                         | 26.5 ms: 1.01x faster                                                    |
| sympy_expand             | 271 ms                                                          | 272 ms: 1.00x slower                                                     |
| deepcopy                 | 220 us                                                          | 221 us: 1.00x slower                                                     |
| json_dumps               | 5.61 ms                                                         | 5.64 ms: 1.01x slower                                                    |
| deepcopy_reduce          | 1.99 us                                                         | 2.01 us: 1.01x slower                                                    |
| hexiom                   | 3.72 ms                                                         | 3.77 ms: 1.01x slower                                                    |
| scimark_sor              | 75.3 ms                                                         | 76.3 ms: 1.01x slower                                                    |
| sympy_str                | 159 ms                                                          | 161 ms: 1.01x slower                                                     |
| create_gc_cycles         | 888 us                                                          | 899 us: 1.01x slower                                                     |
| docutils                 | 1.63 sec                                                        | 1.65 sec: 1.01x slower                                                   |
| 2to3                     | 207 ms                                                          | 210 ms: 1.01x slower                                                     |
| sqlglot_parse            | 748 us                                                          | 760 us: 1.02x slower                                                     |
| sqlglot_transpile        | 955 us                                                          | 971 us: 1.02x slower                                                     |
| scimark_monte_carlo      | 39.1 ms                                                         | 39.8 ms: 1.02x slower                                                    |
| async_tree_io_tg         | 605 ms                                                          | 617 ms: 1.02x slower                                                     |
| async_tree_none          | 218 ms                                                          | 222 ms: 1.02x slower                                                     |
| float                    | 49.7 ms                                                         | 50.7 ms: 1.02x slower                                                    |
| xml_etree_process        | 36.4 ms                                                         | 37.2 ms: 1.02x slower                                                    |
| xml_etree_parse          | 90.9 ms                                                         | 92.8 ms: 1.02x slower                                                    |
| sqlglot_normalize        | 173 ms                                                          | 177 ms: 1.02x slower                                                     |
| logging_silent           | 52.9 ns                                                         | 54.1 ns: 1.02x slower                                                    |
| sqlglot_optimize         | 32.7 ms                                                         | 33.4 ms: 1.02x slower                                                    |
| html5lib                 | 35.0 ms                                                         | 35.8 ms: 1.02x slower                                                    |
| scimark_lu               | 56.6 ms                                                         | 57.9 ms: 1.02x slower                                                    |
| regex_compile            | 78.0 ms                                                         | 79.8 ms: 1.02x slower                                                    |
| coroutines               | 12.8 ms                                                         | 13.1 ms: 1.02x slower                                                    |
| crypto_pyaes             | 45.5 ms                                                         | 46.6 ms: 1.02x slower                                                    |
| async_generators         | 223 ms                                                          | 229 ms: 1.02x slower                                                     |
| xml_etree_generate       | 53.2 ms                                                         | 54.5 ms: 1.02x slower                                                    |
| logging_format           | 6.22 us                                                         | 6.38 us: 1.03x slower                                                    |
| pickle_dict              | 18.1 us                                                         | 18.6 us: 1.03x slower                                                    |
| sympy_integrate          | 12.2 ms                                                         | 12.6 ms: 1.03x slower                                                    |
| pprint_pformat           | 966 ms                                                          | 993 ms: 1.03x slower                                                     |
| comprehensions           | 10.4 us                                                         | 10.7 us: 1.03x slower                                                    |
| xml_etree_iterparse      | 62.3 ms                                                         | 64.1 ms: 1.03x slower                                                    |
| unpickle_pure_python     | 122 us                                                          | 125 us: 1.03x slower                                                     |
| logging_simple           | 5.78 us                                                         | 5.96 us: 1.03x slower                                                    |
| pprint_safe_repr         | 474 ms                                                          | 489 ms: 1.03x slower                                                     |
| sqlite_synth             | 1.60 us                                                         | 1.65 us: 1.03x slower                                                    |
| deltablue                | 1.88 ms                                                         | 1.95 ms: 1.04x slower                                                    |
| go                       | 82.1 ms                                                         | 85.1 ms: 1.04x slower                                                    |
| django_template          | 21.7 ms                                                         | 22.5 ms: 1.04x slower                                                    |
| dulwich_log              | 38.0 ms                                                         | 39.5 ms: 1.04x slower                                                    |
| pyflate                  | 279 ms                                                          | 290 ms: 1.04x slower                                                     |
| meteor_contest           | 69.9 ms                                                         | 72.7 ms: 1.04x slower                                                    |
| tomli_loads              | 1.35 sec                                                        | 1.41 sec: 1.05x slower                                                   |
| nbody                    | 67.6 ms                                                         | 70.8 ms: 1.05x slower                                                    |
| bench_thread_pool        | 768 us                                                          | 809 us: 1.05x slower                                                     |
| nqueens                  | 56.7 ms                                                         | 59.7 ms: 1.05x slower                                                    |
| fannkuch                 | 243 ms                                                          | 257 ms: 1.06x slower                                                     |
| genshi_xml               | 31.6 ms                                                         | 33.5 ms: 1.06x slower                                                    |
| mdp                      | 1.31 sec                                                        | 1.39 sec: 1.06x slower                                                   |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.68 ms: 1.07x slower                                                    |
| async_tree_none_tg       | 202 ms                                                          | 217 ms: 1.08x slower                                                     |
| unpickle_list            | 2.62 us                                                         | 2.83 us: 1.08x slower                                                    |
| pickle_list              | 2.90 us                                                         | 3.16 us: 1.09x slower                                                    |
| telco                    | 4.67 ms                                                         | 5.09 ms: 1.09x slower                                                    |
| generators               | 19.6 ms                                                         | 21.4 ms: 1.09x slower                                                    |
| coverage                 | 42.1 ms                                                         | 46.4 ms: 1.10x slower                                                    |
| genshi_text              | 14.4 ms                                                         | 15.9 ms: 1.11x slower                                                    |
| scimark_fft              | 171 ms                                                          | 190 ms: 1.11x slower                                                     |
| asyncio_tcp_ssl          | 1.48 sec                                                        | 1.69 sec: 1.14x slower                                                   |
| regex_v8                 | 15.8 ms                                                         | 18.3 ms: 1.16x slower                                                    |
| Geometric mean           | (ref)                                                           | 1.02x slower                                                             |

Benchmark hidden because not significant (17): json, mako, chameleon, chaos, richards_super, sympy_sum, mypy2, pickle, pickle_pure_python, pathlib, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, asyncio_tcp, async_tree_io, pylint, async_tree_memoization, async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: unknown