# Results vs. 3.13.0b2

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-amd64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.02x slower
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 223 ms: 1.08x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.64 ms: 1.03x faster                                                       |
| docutils       | 1.63 sec                                                        | 1.68 sec: 1.03x slower                                                      |
| html5lib       | 35.0 ms                                                         | 36.0 ms: 1.03x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 84.0 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                           | 1.03x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 389 ms                                                          | 372 ms: 1.05x faster                                                        |
| async_tree_io           | 588 ms                                                          | 563 ms: 1.04x faster                                                        |
| async_tree_none         | 218 ms                                                          | 213 ms: 1.03x faster                                                        |
| Geometric mean          | (ref)                                                           | 1.01x faster                                                                |

Benchmark hidden because not significant (5): async_tree_io_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 58.8 ms: 1.15x faster                                                       |
| float          | 49.7 ms                                                         | 46.8 ms: 1.06x faster                                                       |
| pidigits       | 150 ms                                                          | 146 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                       |
| regex_dna      | 119 ms                                                          | 121 ms: 1.02x slower                                                        |
| regex_compile  | 78.0 ms                                                         | 83.3 ms: 1.07x slower                                                       |
| Geometric mean | (ref)                                                           | 1.05x slower                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.19 sec: 1.13x faster                                                      |
| json_dumps           | 5.61 ms                                                         | 5.51 ms: 1.02x faster                                                       |
| json_loads           | 14.2 us                                                         | 14.0 us: 1.02x faster                                                       |
| pickle_pure_python   | 175 us                                                          | 175 us: 1.00x faster                                                        |
| xml_etree_generate   | 53.2 ms                                                         | 53.5 ms: 1.01x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 18.4 us: 1.01x slower                                                       |
| unpickle             | 8.40 us                                                         | 8.53 us: 1.02x slower                                                       |
| xml_etree_parse      | 90.9 ms                                                         | 92.4 ms: 1.02x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.67 us: 1.02x slower                                                       |
| pickle               | 7.11 us                                                         | 7.27 us: 1.02x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 130 us: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.00x slower                                                                |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_process, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 22.5 ms: 1.11x slower                                                       |
| python_startup_no_site | 16.2 ms                                                         | 20.4 ms: 1.26x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.18x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 5.61 ms: 1.13x faster                                                       |
| django_template | 21.7 ms                                                         | 22.5 ms: 1.04x slower                                                       |
| genshi_text     | 14.4 ms                                                         | 15.4 ms: 1.07x slower                                                       |
| genshi_xml      | 31.6 ms                                                         | 36.3 ms: 1.15x slower                                                       |
| Geometric mean  | (ref)                                                           | 1.03x slower                                                                |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 69.4 us: 1.45x faster                                                       |
| spectral_norm            | 63.7 ms                                                         | 51.4 ms: 1.24x faster                                                       |
| nbody                    | 67.6 ms                                                         | 58.8 ms: 1.15x faster                                                       |
| mako                     | 6.36 ms                                                         | 5.61 ms: 1.13x faster                                                       |
| tomli_loads              | 1.35 sec                                                        | 1.19 sec: 1.13x faster                                                      |
| pycparser                | 754 ms                                                          | 671 ms: 1.12x faster                                                        |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.24 ms: 1.12x faster                                                       |
| fannkuch                 | 243 ms                                                          | 229 ms: 1.06x faster                                                        |
| float                    | 49.7 ms                                                         | 46.8 ms: 1.06x faster                                                       |
| pylint                   | 205 ms                                                          | 194 ms: 1.05x faster                                                        |
| async_tree_cpu_io_mixed  | 389 ms                                                          | 372 ms: 1.05x faster                                                        |
| async_tree_io            | 588 ms                                                          | 563 ms: 1.04x faster                                                        |
| create_gc_cycles         | 888 us                                                          | 853 us: 1.04x faster                                                        |
| deepcopy_reduce          | 1.99 us                                                         | 1.92 us: 1.04x faster                                                       |
| chameleon                | 4.80 ms                                                         | 4.64 ms: 1.03x faster                                                       |
| async_tree_none          | 218 ms                                                          | 213 ms: 1.03x faster                                                        |
| pidigits                 | 150 ms                                                          | 146 ms: 1.02x faster                                                        |
| scimark_fft              | 171 ms                                                          | 167 ms: 1.02x faster                                                        |
| deepcopy_memo            | 22.1 us                                                         | 21.6 us: 1.02x faster                                                       |
| crypto_pyaes             | 45.5 ms                                                         | 44.6 ms: 1.02x faster                                                       |
| json_dumps               | 5.61 ms                                                         | 5.51 ms: 1.02x faster                                                       |
| json_loads               | 14.2 us                                                         | 14.0 us: 1.02x faster                                                       |
| gc_traversal             | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                       |
| sqlite_synth             | 1.60 us                                                         | 1.58 us: 1.01x faster                                                       |
| pickle_pure_python       | 175 us                                                          | 175 us: 1.00x faster                                                        |
| generators               | 19.6 ms                                                         | 19.5 ms: 1.00x faster                                                       |
| xml_etree_generate       | 53.2 ms                                                         | 53.5 ms: 1.01x slower                                                       |
| scimark_monte_carlo      | 39.1 ms                                                         | 39.4 ms: 1.01x slower                                                       |
| aiohttp                  | 889 us                                                          | 898 us: 1.01x slower                                                        |
| logging_format           | 6.22 us                                                         | 6.29 us: 1.01x slower                                                       |
| regex_effbot             | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                       |
| pickle_dict              | 18.1 us                                                         | 18.4 us: 1.01x slower                                                       |
| chaos                    | 38.4 ms                                                         | 38.9 ms: 1.01x slower                                                       |
| unpickle                 | 8.40 us                                                         | 8.53 us: 1.02x slower                                                       |
| telco                    | 4.67 ms                                                         | 4.74 ms: 1.02x slower                                                       |
| regex_dna                | 119 ms                                                          | 121 ms: 1.02x slower                                                        |
| deepcopy                 | 220 us                                                          | 223 us: 1.02x slower                                                        |
| xml_etree_parse          | 90.9 ms                                                         | 92.4 ms: 1.02x slower                                                       |
| unpickle_list            | 2.62 us                                                         | 2.67 us: 1.02x slower                                                       |
| logging_simple           | 5.78 us                                                         | 5.91 us: 1.02x slower                                                       |
| pickle                   | 7.11 us                                                         | 7.27 us: 1.02x slower                                                       |
| pathlib                  | 75.9 ms                                                         | 77.8 ms: 1.03x slower                                                       |
| tornado_http             | 81.8 ms                                                         | 84.0 ms: 1.03x slower                                                       |
| html5lib                 | 35.0 ms                                                         | 36.0 ms: 1.03x slower                                                       |
| sympy_sum                | 84.4 ms                                                         | 86.8 ms: 1.03x slower                                                       |
| sqlglot_parse            | 748 us                                                          | 772 us: 1.03x slower                                                        |
| sqlglot_transpile        | 955 us                                                          | 986 us: 1.03x slower                                                        |
| docutils                 | 1.63 sec                                                        | 1.68 sec: 1.03x slower                                                      |
| coroutines               | 12.8 ms                                                         | 13.2 ms: 1.04x slower                                                       |
| sympy_str                | 159 ms                                                          | 165 ms: 1.04x slower                                                        |
| django_template          | 21.7 ms                                                         | 22.5 ms: 1.04x slower                                                       |
| meteor_contest           | 69.9 ms                                                         | 73.2 ms: 1.05x slower                                                       |
| sympy_expand             | 271 ms                                                          | 284 ms: 1.05x slower                                                        |
| sqlglot_normalize        | 173 ms                                                          | 184 ms: 1.06x slower                                                        |
| unpickle_pure_python     | 122 us                                                          | 130 us: 1.07x slower                                                        |
| dulwich_log              | 38.0 ms                                                         | 40.6 ms: 1.07x slower                                                       |
| regex_compile            | 78.0 ms                                                         | 83.3 ms: 1.07x slower                                                       |
| deltablue                | 1.88 ms                                                         | 2.01 ms: 1.07x slower                                                       |
| scimark_sor              | 75.3 ms                                                         | 80.5 ms: 1.07x slower                                                       |
| bench_thread_pool        | 768 us                                                          | 822 us: 1.07x slower                                                        |
| mypy2                    | 418 ms                                                          | 448 ms: 1.07x slower                                                        |
| genshi_text              | 14.4 ms                                                         | 15.4 ms: 1.07x slower                                                       |
| 2to3                     | 207 ms                                                          | 223 ms: 1.08x slower                                                        |
| sympy_integrate          | 12.2 ms                                                         | 13.2 ms: 1.08x slower                                                       |
| mdp                      | 1.31 sec                                                        | 1.41 sec: 1.08x slower                                                      |
| richards_super           | 30.2 ms                                                         | 32.7 ms: 1.08x slower                                                       |
| sqlglot_optimize         | 32.7 ms                                                         | 35.5 ms: 1.08x slower                                                       |
| richards                 | 26.7 ms                                                         | 29.1 ms: 1.09x slower                                                       |
| comprehensions           | 10.4 us                                                         | 11.3 us: 1.09x slower                                                       |
| nqueens                  | 56.7 ms                                                         | 61.9 ms: 1.09x slower                                                       |
| bench_mp_pool            | 64.8 ms                                                         | 70.8 ms: 1.09x slower                                                       |
| raytrace                 | 162 ms                                                          | 178 ms: 1.09x slower                                                        |
| thrift                   | 8.11 ms                                                         | 8.91 ms: 1.10x slower                                                       |
| python_startup           | 20.3 ms                                                         | 22.5 ms: 1.11x slower                                                       |
| async_generators         | 223 ms                                                          | 248 ms: 1.11x slower                                                        |
| coverage                 | 42.1 ms                                                         | 47.0 ms: 1.12x slower                                                       |
| go                       | 82.1 ms                                                         | 93.0 ms: 1.13x slower                                                       |
| genshi_xml               | 31.6 ms                                                         | 36.3 ms: 1.15x slower                                                       |
| json                     | 3.19 ms                                                         | 3.88 ms: 1.22x slower                                                       |
| scimark_lu               | 56.6 ms                                                         | 69.1 ms: 1.22x slower                                                       |
| hexiom                   | 3.72 ms                                                         | 4.61 ms: 1.24x slower                                                       |
| python_startup_no_site   | 16.2 ms                                                         | 20.4 ms: 1.26x slower                                                       |
| Geometric mean           | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (15): async_tree_io_tg, async_tree_none_tg, logging_silent, async_tree_cpu_io_mixed_tg, xml_etree_iterparse, xml_etree_process, pprint_safe_repr, asyncio_tcp, async_tree_memoization, pprint_pformat, async_tree_memoization_tg, pyflate, pickle_list, asyncio_tcp_ssl, regex_v8
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: unpack_sequence

# HPT report

- Reliability score: 99.94% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown