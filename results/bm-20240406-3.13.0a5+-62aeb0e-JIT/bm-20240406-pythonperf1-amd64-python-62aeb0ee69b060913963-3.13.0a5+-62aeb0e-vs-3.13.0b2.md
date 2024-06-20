# Results vs. 3.13.0b2

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.01x slower
- HPT reliability: 99.78%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 221 ms: 1.07x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.70 ms: 1.02x faster                                                       |
| docutils       | 1.63 sec                                                        | 1.70 sec: 1.05x slower                                                      |
| html5lib       | 35.0 ms                                                         | 35.4 ms: 1.01x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 83.6 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|--------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg | 202 ms                                                          | 212 ms: 1.05x slower                                                        |
| Geometric mean     | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (7): async_tree_io, async_tree_cpu_io_mixed, async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 57.8 ms: 1.17x faster                                                       |
| float          | 49.7 ms                                                         | 46.8 ms: 1.06x faster                                                       |
| pidigits       | 150 ms                                                          | 146 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.1 ms: 1.12x faster                                                       |
| regex_effbot   | 1.58 ms                                                         | 1.55 ms: 1.02x faster                                                       |
| regex_compile  | 78.0 ms                                                         | 87.0 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                           | 1.00x faster                                                                |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.19 sec: 1.14x faster                                                      |
| json_loads           | 14.2 us                                                         | 13.7 us: 1.04x faster                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 60.6 ms: 1.03x faster                                                       |
| pickle_pure_python   | 175 us                                                          | 172 us: 1.02x faster                                                        |
| pickle_list          | 2.90 us                                                         | 2.85 us: 1.02x faster                                                       |
| json_dumps           | 5.61 ms                                                         | 5.54 ms: 1.01x faster                                                       |
| pickle               | 7.11 us                                                         | 7.39 us: 1.04x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 19.0 us: 1.05x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 129 us: 1.06x slower                                                        |
| unpickle             | 8.40 us                                                         | 9.09 us: 1.08x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.90 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (3): xml_etree_generate, xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 22.2 ms: 1.09x slower                                                       |
| python_startup_no_site | 16.2 ms                                                         | 20.2 ms: 1.25x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.17x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 6.36 ms                                                         | 5.63 ms: 1.13x faster                                                       |
| genshi_text    | 14.4 ms                                                         | 15.6 ms: 1.09x slower                                                       |
| genshi_xml     | 31.6 ms                                                         | 34.8 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 72.5 us: 1.39x faster                                                       |
| spectral_norm            | 63.7 ms                                                         | 50.4 ms: 1.27x faster                                                       |
| nbody                    | 67.6 ms                                                         | 57.8 ms: 1.17x faster                                                       |
| tomli_loads              | 1.35 sec                                                        | 1.19 sec: 1.14x faster                                                      |
| mako                     | 6.36 ms                                                         | 5.63 ms: 1.13x faster                                                       |
| regex_v8                 | 15.8 ms                                                         | 14.1 ms: 1.12x faster                                                       |
| json                     | 3.19 ms                                                         | 2.89 ms: 1.10x faster                                                       |
| pycparser                | 754 ms                                                          | 687 ms: 1.10x faster                                                        |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.30 ms: 1.09x faster                                                       |
| float                    | 49.7 ms                                                         | 46.8 ms: 1.06x faster                                                       |
| pylint                   | 205 ms                                                          | 194 ms: 1.06x faster                                                        |
| fannkuch                 | 243 ms                                                          | 231 ms: 1.05x faster                                                        |
| deepcopy_memo            | 22.1 us                                                         | 21.0 us: 1.05x faster                                                       |
| crypto_pyaes             | 45.5 ms                                                         | 43.6 ms: 1.04x faster                                                       |
| pyflate                  | 279 ms                                                          | 268 ms: 1.04x faster                                                        |
| json_loads               | 14.2 us                                                         | 13.7 us: 1.04x faster                                                       |
| xml_etree_iterparse      | 62.3 ms                                                         | 60.6 ms: 1.03x faster                                                       |
| pidigits                 | 150 ms                                                          | 146 ms: 1.02x faster                                                        |
| pickle_pure_python       | 175 us                                                          | 172 us: 1.02x faster                                                        |
| chameleon                | 4.80 ms                                                         | 4.70 ms: 1.02x faster                                                       |
| deepcopy_reduce          | 1.99 us                                                         | 1.95 us: 1.02x faster                                                       |
| regex_effbot             | 1.58 ms                                                         | 1.55 ms: 1.02x faster                                                       |
| logging_format           | 6.22 us                                                         | 6.11 us: 1.02x faster                                                       |
| pickle_list              | 2.90 us                                                         | 2.85 us: 1.02x faster                                                       |
| scimark_fft              | 171 ms                                                          | 169 ms: 1.01x faster                                                        |
| json_dumps               | 5.61 ms                                                         | 5.54 ms: 1.01x faster                                                       |
| logging_simple           | 5.78 us                                                         | 5.72 us: 1.01x faster                                                       |
| gc_traversal             | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                       |
| scimark_monte_carlo      | 39.1 ms                                                         | 38.7 ms: 1.01x faster                                                       |
| richards                 | 26.7 ms                                                         | 26.5 ms: 1.01x faster                                                       |
| generators               | 19.6 ms                                                         | 19.6 ms: 1.00x slower                                                       |
| html5lib                 | 35.0 ms                                                         | 35.4 ms: 1.01x slower                                                       |
| pathlib                  | 75.9 ms                                                         | 76.8 ms: 1.01x slower                                                       |
| logging_silent           | 52.9 ns                                                         | 53.6 ns: 1.01x slower                                                       |
| pprint_pformat           | 966 ms                                                          | 979 ms: 1.01x slower                                                        |
| aiohttp                  | 889 us                                                          | 900 us: 1.01x slower                                                        |
| raytrace                 | 162 ms                                                          | 164 ms: 1.01x slower                                                        |
| telco                    | 4.67 ms                                                         | 4.74 ms: 1.01x slower                                                       |
| pprint_safe_repr         | 474 ms                                                          | 481 ms: 1.02x slower                                                        |
| coroutines               | 12.8 ms                                                         | 13.0 ms: 1.02x slower                                                       |
| tornado_http             | 81.8 ms                                                         | 83.6 ms: 1.02x slower                                                       |
| bench_thread_pool        | 768 us                                                          | 795 us: 1.04x slower                                                        |
| sqlglot_normalize        | 173 ms                                                          | 180 ms: 1.04x slower                                                        |
| meteor_contest           | 69.9 ms                                                         | 72.5 ms: 1.04x slower                                                       |
| pickle                   | 7.11 us                                                         | 7.39 us: 1.04x slower                                                       |
| sqlglot_transpile        | 955 us                                                          | 994 us: 1.04x slower                                                        |
| sympy_sum                | 84.4 ms                                                         | 88.0 ms: 1.04x slower                                                       |
| docutils                 | 1.63 sec                                                        | 1.70 sec: 1.05x slower                                                      |
| pickle_dict              | 18.1 us                                                         | 19.0 us: 1.05x slower                                                       |
| comprehensions           | 10.4 us                                                         | 10.9 us: 1.05x slower                                                       |
| sqlglot_parse            | 748 us                                                          | 785 us: 1.05x slower                                                        |
| async_tree_none_tg       | 202 ms                                                          | 212 ms: 1.05x slower                                                        |
| async_generators         | 223 ms                                                          | 235 ms: 1.05x slower                                                        |
| sympy_expand             | 271 ms                                                          | 285 ms: 1.05x slower                                                        |
| thrift                   | 8.11 ms                                                         | 8.54 ms: 1.05x slower                                                       |
| sympy_str                | 159 ms                                                          | 168 ms: 1.06x slower                                                        |
| unpickle_pure_python     | 122 us                                                          | 129 us: 1.06x slower                                                        |
| dulwich_log              | 38.0 ms                                                         | 40.4 ms: 1.06x slower                                                       |
| 2to3                     | 207 ms                                                          | 221 ms: 1.07x slower                                                        |
| sqlglot_optimize         | 32.7 ms                                                         | 35.0 ms: 1.07x slower                                                       |
| asyncio_tcp_ssl          | 1.48 sec                                                        | 1.58 sec: 1.07x slower                                                      |
| mypy2                    | 418 ms                                                          | 449 ms: 1.07x slower                                                        |
| bench_mp_pool            | 64.8 ms                                                         | 69.9 ms: 1.08x slower                                                       |
| unpickle                 | 8.40 us                                                         | 9.09 us: 1.08x slower                                                       |
| nqueens                  | 56.7 ms                                                         | 61.5 ms: 1.08x slower                                                       |
| genshi_text              | 14.4 ms                                                         | 15.6 ms: 1.09x slower                                                       |
| sympy_integrate          | 12.2 ms                                                         | 13.3 ms: 1.09x slower                                                       |
| python_startup           | 20.3 ms                                                         | 22.2 ms: 1.09x slower                                                       |
| genshi_xml               | 31.6 ms                                                         | 34.8 ms: 1.10x slower                                                       |
| scimark_sor              | 75.3 ms                                                         | 83.4 ms: 1.11x slower                                                       |
| unpickle_list            | 2.62 us                                                         | 2.90 us: 1.11x slower                                                       |
| regex_compile            | 78.0 ms                                                         | 87.0 ms: 1.12x slower                                                       |
| go                       | 82.1 ms                                                         | 92.0 ms: 1.12x slower                                                       |
| mdp                      | 1.31 sec                                                        | 1.47 sec: 1.12x slower                                                      |
| coverage                 | 42.1 ms                                                         | 47.2 ms: 1.12x slower                                                       |
| deltablue                | 1.88 ms                                                         | 2.15 ms: 1.14x slower                                                       |
| hexiom                   | 3.72 ms                                                         | 4.45 ms: 1.20x slower                                                       |
| python_startup_no_site   | 16.2 ms                                                         | 20.2 ms: 1.25x slower                                                       |
| scimark_lu               | 56.6 ms                                                         | 73.2 ms: 1.29x slower                                                       |
| Geometric mean           | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (17): async_tree_io, async_tree_cpu_io_mixed, sqlite_synth, deepcopy, async_tree_none, xml_etree_generate, richards_super, xml_etree_parse, async_tree_io_tg, regex_dna, async_tree_cpu_io_mixed_tg, chaos, async_tree_memoization, xml_etree_process, create_gc_cycles, async_tree_memoization_tg, asyncio_tcp
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 99.78% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown