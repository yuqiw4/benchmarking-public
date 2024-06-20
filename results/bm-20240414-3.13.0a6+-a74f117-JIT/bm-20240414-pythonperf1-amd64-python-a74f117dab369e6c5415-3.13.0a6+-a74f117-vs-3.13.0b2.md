# Results vs. 3.13.0b2

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.01x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 218 ms: 1.05x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.67 ms: 1.03x faster                                                       |
| docutils       | 1.63 sec                                                        | 1.68 sec: 1.04x slower                                                      |
| html5lib       | 35.0 ms                                                         | 36.0 ms: 1.03x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 83.0 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|--------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg | 202 ms                                                          | 214 ms: 1.06x slower                                                        |
| Geometric mean     | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_io, async_tree_none, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 58.3 ms: 1.16x faster                                                       |
| float          | 49.7 ms                                                         | 46.7 ms: 1.07x faster                                                       |
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                       |
| regex_dna      | 119 ms                                                          | 120 ms: 1.01x slower                                                        |
| regex_compile  | 78.0 ms                                                         | 86.8 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.18 sec: 1.14x faster                                                      |
| pickle_pure_python   | 175 us                                                          | 171 us: 1.03x faster                                                        |
| xml_etree_iterparse  | 62.3 ms                                                         | 60.9 ms: 1.02x faster                                                       |
| json_loads           | 14.2 us                                                         | 13.9 us: 1.02x faster                                                       |
| json_dumps           | 5.61 ms                                                         | 5.52 ms: 1.02x faster                                                       |
| xml_etree_parse      | 90.9 ms                                                         | 90.0 ms: 1.01x faster                                                       |
| unpickle_pure_python | 122 us                                                          | 123 us: 1.01x slower                                                        |
| xml_etree_process    | 36.4 ms                                                         | 37.0 ms: 1.01x slower                                                       |
| pickle               | 7.11 us                                                         | 7.23 us: 1.02x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 18.5 us: 1.02x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.74 us: 1.05x slower                                                       |
| unpickle             | 8.40 us                                                         | 8.80 us: 1.05x slower                                                       |
| Geometric mean       | (ref)                                                           | 1.01x faster                                                                |

Benchmark hidden because not significant (2): xml_etree_generate, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 21.4 ms: 1.05x slower                                                       |
| python_startup_no_site | 16.2 ms                                                         | 17.8 ms: 1.10x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 6.36 ms                                                         | 5.72 ms: 1.11x faster                                                       |
| genshi_text    | 14.4 ms                                                         | 15.5 ms: 1.08x slower                                                       |
| genshi_xml     | 31.6 ms                                                         | 34.8 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 71.1 us: 1.42x faster                                                       |
| spectral_norm            | 63.7 ms                                                         | 51.3 ms: 1.24x faster                                                       |
| nbody                    | 67.6 ms                                                         | 58.3 ms: 1.16x faster                                                       |
| tomli_loads              | 1.35 sec                                                        | 1.18 sec: 1.14x faster                                                      |
| mako                     | 6.36 ms                                                         | 5.72 ms: 1.11x faster                                                       |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.27 ms: 1.10x faster                                                       |
| fannkuch                 | 243 ms                                                          | 226 ms: 1.08x faster                                                        |
| float                    | 49.7 ms                                                         | 46.7 ms: 1.07x faster                                                       |
| pylint                   | 205 ms                                                          | 194 ms: 1.05x faster                                                        |
| deepcopy_memo            | 22.1 us                                                         | 21.0 us: 1.05x faster                                                       |
| scimark_fft              | 171 ms                                                          | 165 ms: 1.04x faster                                                        |
| pyflate                  | 279 ms                                                          | 269 ms: 1.04x faster                                                        |
| pickle_pure_python       | 175 us                                                          | 171 us: 1.03x faster                                                        |
| chameleon                | 4.80 ms                                                         | 4.67 ms: 1.03x faster                                                       |
| crypto_pyaes             | 45.5 ms                                                         | 44.3 ms: 1.03x faster                                                       |
| deepcopy_reduce          | 1.99 us                                                         | 1.94 us: 1.03x faster                                                       |
| pprint_pformat           | 966 ms                                                          | 943 ms: 1.02x faster                                                        |
| xml_etree_iterparse      | 62.3 ms                                                         | 60.9 ms: 1.02x faster                                                       |
| json_loads               | 14.2 us                                                         | 13.9 us: 1.02x faster                                                       |
| pidigits                 | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| scimark_monte_carlo      | 39.1 ms                                                         | 38.5 ms: 1.02x faster                                                       |
| json_dumps               | 5.61 ms                                                         | 5.52 ms: 1.02x faster                                                       |
| pathlib                  | 75.9 ms                                                         | 74.8 ms: 1.01x faster                                                       |
| xml_etree_parse          | 90.9 ms                                                         | 90.0 ms: 1.01x faster                                                       |
| deepcopy                 | 220 us                                                          | 218 us: 1.01x faster                                                        |
| sqlite_synth             | 1.60 us                                                         | 1.58 us: 1.01x faster                                                       |
| gc_traversal             | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                       |
| pprint_safe_repr         | 474 ms                                                          | 470 ms: 1.01x faster                                                        |
| logging_format           | 6.22 us                                                         | 6.26 us: 1.01x slower                                                       |
| regex_effbot             | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                       |
| generators               | 19.6 ms                                                         | 19.8 ms: 1.01x slower                                                       |
| aiohttp                  | 889 us                                                          | 898 us: 1.01x slower                                                        |
| unpickle_pure_python     | 122 us                                                          | 123 us: 1.01x slower                                                        |
| richards                 | 26.7 ms                                                         | 27.0 ms: 1.01x slower                                                       |
| chaos                    | 38.4 ms                                                         | 38.9 ms: 1.01x slower                                                       |
| regex_dna                | 119 ms                                                          | 120 ms: 1.01x slower                                                        |
| richards_super           | 30.2 ms                                                         | 30.6 ms: 1.01x slower                                                       |
| tornado_http             | 81.8 ms                                                         | 83.0 ms: 1.01x slower                                                       |
| xml_etree_process        | 36.4 ms                                                         | 37.0 ms: 1.01x slower                                                       |
| pickle                   | 7.11 us                                                         | 7.23 us: 1.02x slower                                                       |
| pickle_dict              | 18.1 us                                                         | 18.5 us: 1.02x slower                                                       |
| coroutines               | 12.8 ms                                                         | 13.0 ms: 1.02x slower                                                       |
| meteor_contest           | 69.9 ms                                                         | 71.7 ms: 1.03x slower                                                       |
| html5lib                 | 35.0 ms                                                         | 36.0 ms: 1.03x slower                                                       |
| bench_thread_pool        | 768 us                                                          | 791 us: 1.03x slower                                                        |
| comprehensions           | 10.4 us                                                         | 10.7 us: 1.03x slower                                                       |
| sqlglot_normalize        | 173 ms                                                          | 179 ms: 1.03x slower                                                        |
| telco                    | 4.67 ms                                                         | 4.83 ms: 1.03x slower                                                       |
| docutils                 | 1.63 sec                                                        | 1.68 sec: 1.04x slower                                                      |
| bench_mp_pool            | 64.8 ms                                                         | 67.2 ms: 1.04x slower                                                       |
| logging_silent           | 52.9 ns                                                         | 54.9 ns: 1.04x slower                                                       |
| sqlglot_transpile        | 955 us                                                          | 995 us: 1.04x slower                                                        |
| unpickle_list            | 2.62 us                                                         | 2.74 us: 1.05x slower                                                       |
| sqlglot_parse            | 748 us                                                          | 783 us: 1.05x slower                                                        |
| sympy_sum                | 84.4 ms                                                         | 88.3 ms: 1.05x slower                                                       |
| unpickle                 | 8.40 us                                                         | 8.80 us: 1.05x slower                                                       |
| raytrace                 | 162 ms                                                          | 170 ms: 1.05x slower                                                        |
| python_startup           | 20.3 ms                                                         | 21.4 ms: 1.05x slower                                                       |
| 2to3                     | 207 ms                                                          | 218 ms: 1.05x slower                                                        |
| sympy_expand             | 271 ms                                                          | 286 ms: 1.06x slower                                                        |
| sympy_str                | 159 ms                                                          | 168 ms: 1.06x slower                                                        |
| async_tree_none_tg       | 202 ms                                                          | 214 ms: 1.06x slower                                                        |
| sqlglot_optimize         | 32.7 ms                                                         | 34.7 ms: 1.06x slower                                                       |
| dulwich_log              | 38.0 ms                                                         | 40.5 ms: 1.07x slower                                                       |
| asyncio_tcp_ssl          | 1.48 sec                                                        | 1.58 sec: 1.07x slower                                                      |
| nqueens                  | 56.7 ms                                                         | 60.5 ms: 1.07x slower                                                       |
| mypy2                    | 418 ms                                                          | 447 ms: 1.07x slower                                                        |
| async_generators         | 223 ms                                                          | 240 ms: 1.08x slower                                                        |
| genshi_text              | 14.4 ms                                                         | 15.5 ms: 1.08x slower                                                       |
| thrift                   | 8.11 ms                                                         | 8.76 ms: 1.08x slower                                                       |
| sympy_integrate          | 12.2 ms                                                         | 13.3 ms: 1.09x slower                                                       |
| python_startup_no_site   | 16.2 ms                                                         | 17.8 ms: 1.10x slower                                                       |
| genshi_xml               | 31.6 ms                                                         | 34.8 ms: 1.10x slower                                                       |
| coverage                 | 42.1 ms                                                         | 46.4 ms: 1.10x slower                                                       |
| scimark_sor              | 75.3 ms                                                         | 83.1 ms: 1.10x slower                                                       |
| regex_compile            | 78.0 ms                                                         | 86.8 ms: 1.11x slower                                                       |
| go                       | 82.1 ms                                                         | 91.8 ms: 1.12x slower                                                       |
| mdp                      | 1.31 sec                                                        | 1.53 sec: 1.17x slower                                                      |
| deltablue                | 1.88 ms                                                         | 2.20 ms: 1.17x slower                                                       |
| hexiom                   | 3.72 ms                                                         | 4.45 ms: 1.19x slower                                                       |
| scimark_lu               | 56.6 ms                                                         | 73.2 ms: 1.29x slower                                                       |
| Geometric mean           | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (15): regex_v8, pycparser, create_gc_cycles, xml_etree_generate, logging_simple, pickle_list, async_tree_io_tg, async_tree_io, async_tree_none, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization, json, asyncio_tcp, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown