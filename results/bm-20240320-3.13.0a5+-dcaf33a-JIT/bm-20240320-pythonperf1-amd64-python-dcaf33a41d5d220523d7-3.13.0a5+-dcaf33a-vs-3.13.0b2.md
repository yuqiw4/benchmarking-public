# Results vs. 3.13.0b2

- fork: python
- ref: dcaf33a41d5d220523d7
- machine: windows-amd64
- commit hash: dcaf33a
- commit date: 2024-03-20
- overall geometric mean: 1.27x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 235 ms: 1.13x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.67 ms: 1.03x faster                                                       |
| docutils       | 1.63 sec                                                        | 2.43 sec: 1.49x slower                                                      |
| html5lib       | 35.0 ms                                                         | 40.1 ms: 1.15x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 86.9 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                           | 1.15x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 389 ms                                                          | 2.25 sec: 5.79x slower                                                      |
| async_tree_cpu_io_mixed_tg | 382 ms                                                          | 2.46 sec: 6.43x slower                                                      |
| async_tree_none            | 218 ms                                                          | 1.81 sec: 8.31x slower                                                      |
| async_tree_memoization     | 264 ms                                                          | 2.32 sec: 8.78x slower                                                      |
| async_tree_memoization_tg  | 258 ms                                                          | 2.53 sec: 9.79x slower                                                      |
| async_tree_none_tg         | 202 ms                                                          | 1.99 sec: 9.88x slower                                                      |
| async_tree_io              | 588 ms                                                          | 7.30 sec: 12.43x slower                                                     |
| async_tree_io_tg           | 605 ms                                                          | 7.85 sec: 12.97x slower                                                     |
| Geometric mean             | (ref)                                                           | 8.98x slower                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 58.4 ms: 1.16x faster                                                       |
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| float          | 49.7 ms                                                         | 81.6 ms: 1.64x slower                                                       |
| Geometric mean | (ref)                                                           | 1.11x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.6 ms: 1.08x faster                                                       |
| regex_effbot   | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                       |
| regex_dna      | 119 ms                                                          | 120 ms: 1.01x slower                                                        |
| regex_compile  | 78.0 ms                                                         | 82.8 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                           | 1.00x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.21 sec: 1.12x faster                                                      |
| json_loads           | 14.2 us                                                         | 13.6 us: 1.04x faster                                                       |
| pickle_pure_python   | 175 us                                                          | 177 us: 1.01x slower                                                        |
| unpickle             | 8.40 us                                                         | 8.59 us: 1.02x slower                                                       |
| pickle_list          | 2.90 us                                                         | 3.00 us: 1.03x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.73 us: 1.04x slower                                                       |
| pickle               | 7.11 us                                                         | 7.42 us: 1.04x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 128 us: 1.05x slower                                                        |
| pickle_dict          | 18.1 us                                                         | 19.2 us: 1.06x slower                                                       |
| xml_etree_process    | 36.4 ms                                                         | 40.6 ms: 1.11x slower                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 59.7 ms: 1.12x slower                                                       |
| xml_etree_parse      | 90.9 ms                                                         | 123 ms: 1.35x slower                                                        |
| xml_etree_iterparse  | 62.3 ms                                                         | 94.3 ms: 1.51x slower                                                       |
| Geometric mean       | (ref)                                                           | 1.08x slower                                                                |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 23.9 ms: 1.18x slower                                                       |
| python_startup_no_site | 16.2 ms                                                         | 21.6 ms: 1.33x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.25x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 5.58 ms: 1.14x faster                                                       |
| django_template | 21.7 ms                                                         | 21.9 ms: 1.01x slower                                                       |
| genshi_text     | 14.4 ms                                                         | 15.7 ms: 1.09x slower                                                       |
| genshi_xml      | 31.6 ms                                                         | 37.3 ms: 1.18x slower                                                       |
| Geometric mean  | (ref)                                                           | 1.03x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 101 us                                                          | 71.2 us: 1.42x faster                                                       |
| spectral_norm              | 63.7 ms                                                         | 51.3 ms: 1.24x faster                                                       |
| create_gc_cycles           | 888 us                                                          | 757 us: 1.17x faster                                                        |
| nbody                      | 67.6 ms                                                         | 58.4 ms: 1.16x faster                                                       |
| mako                       | 6.36 ms                                                         | 5.58 ms: 1.14x faster                                                       |
| gc_traversal               | 1.55 ms                                                         | 1.37 ms: 1.13x faster                                                       |
| scimark_sparse_mat_mult    | 2.50 ms                                                         | 2.23 ms: 1.12x faster                                                       |
| tomli_loads                | 1.35 sec                                                        | 1.21 sec: 1.12x faster                                                      |
| json                       | 3.19 ms                                                         | 2.86 ms: 1.11x faster                                                       |
| regex_v8                   | 15.8 ms                                                         | 14.6 ms: 1.08x faster                                                       |
| fannkuch                   | 243 ms                                                          | 228 ms: 1.07x faster                                                        |
| crypto_pyaes               | 45.5 ms                                                         | 43.3 ms: 1.05x faster                                                       |
| json_loads                 | 14.2 us                                                         | 13.6 us: 1.04x faster                                                       |
| deepcopy_memo              | 22.1 us                                                         | 21.2 us: 1.04x faster                                                       |
| chameleon                  | 4.80 ms                                                         | 4.67 ms: 1.03x faster                                                       |
| deepcopy_reduce            | 1.99 us                                                         | 1.94 us: 1.03x faster                                                       |
| pidigits                   | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| scimark_fft                | 171 ms                                                          | 168 ms: 1.02x faster                                                        |
| regex_effbot               | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                       |
| sqlite_synth               | 1.60 us                                                         | 1.58 us: 1.01x faster                                                       |
| pyflate                    | 279 ms                                                          | 280 ms: 1.01x slower                                                        |
| pickle_pure_python         | 175 us                                                          | 177 us: 1.01x slower                                                        |
| django_template            | 21.7 ms                                                         | 21.9 ms: 1.01x slower                                                       |
| pprint_safe_repr           | 474 ms                                                          | 479 ms: 1.01x slower                                                        |
| richards_super             | 30.2 ms                                                         | 30.5 ms: 1.01x slower                                                       |
| regex_dna                  | 119 ms                                                          | 120 ms: 1.01x slower                                                        |
| logging_simple             | 5.78 us                                                         | 5.88 us: 1.02x slower                                                       |
| telco                      | 4.67 ms                                                         | 4.74 ms: 1.02x slower                                                       |
| pathlib                    | 75.9 ms                                                         | 77.1 ms: 1.02x slower                                                       |
| pprint_pformat             | 966 ms                                                          | 983 ms: 1.02x slower                                                        |
| richards                   | 26.7 ms                                                         | 27.2 ms: 1.02x slower                                                       |
| unpickle                   | 8.40 us                                                         | 8.59 us: 1.02x slower                                                       |
| logging_format             | 6.22 us                                                         | 6.37 us: 1.02x slower                                                       |
| sympy_sum                  | 84.4 ms                                                         | 86.7 ms: 1.03x slower                                                       |
| generators                 | 19.6 ms                                                         | 20.2 ms: 1.03x slower                                                       |
| pickle_list                | 2.90 us                                                         | 3.00 us: 1.03x slower                                                       |
| logging_silent             | 52.9 ns                                                         | 54.8 ns: 1.03x slower                                                       |
| comprehensions             | 10.4 us                                                         | 10.7 us: 1.04x slower                                                       |
| sympy_str                  | 159 ms                                                          | 165 ms: 1.04x slower                                                        |
| chaos                      | 38.4 ms                                                         | 39.9 ms: 1.04x slower                                                       |
| unpickle_list              | 2.62 us                                                         | 2.73 us: 1.04x slower                                                       |
| coroutines                 | 12.8 ms                                                         | 13.3 ms: 1.04x slower                                                       |
| pickle                     | 7.11 us                                                         | 7.42 us: 1.04x slower                                                       |
| sqlglot_normalize          | 173 ms                                                          | 181 ms: 1.05x slower                                                        |
| sympy_expand               | 271 ms                                                          | 285 ms: 1.05x slower                                                        |
| unpickle_pure_python       | 122 us                                                          | 128 us: 1.05x slower                                                        |
| scimark_monte_carlo        | 39.1 ms                                                         | 41.2 ms: 1.05x slower                                                       |
| pickle_dict                | 18.1 us                                                         | 19.2 us: 1.06x slower                                                       |
| aiohttp                    | 889 us                                                          | 941 us: 1.06x slower                                                        |
| regex_compile              | 78.0 ms                                                         | 82.8 ms: 1.06x slower                                                       |
| tornado_http               | 81.8 ms                                                         | 86.9 ms: 1.06x slower                                                       |
| sympy_integrate            | 12.2 ms                                                         | 13.0 ms: 1.06x slower                                                       |
| nqueens                    | 56.7 ms                                                         | 60.3 ms: 1.06x slower                                                       |
| meteor_contest             | 69.9 ms                                                         | 74.5 ms: 1.07x slower                                                       |
| scimark_sor                | 75.3 ms                                                         | 81.4 ms: 1.08x slower                                                       |
| bench_thread_pool          | 768 us                                                          | 835 us: 1.09x slower                                                        |
| dulwich_log                | 38.0 ms                                                         | 41.5 ms: 1.09x slower                                                       |
| genshi_text                | 14.4 ms                                                         | 15.7 ms: 1.09x slower                                                       |
| thrift                     | 8.11 ms                                                         | 8.90 ms: 1.10x slower                                                       |
| pycparser                  | 754 ms                                                          | 828 ms: 1.10x slower                                                        |
| bench_mp_pool              | 64.8 ms                                                         | 71.5 ms: 1.10x slower                                                       |
| sqlglot_optimize           | 32.7 ms                                                         | 36.2 ms: 1.11x slower                                                       |
| sqlglot_transpile          | 955 us                                                          | 1.06 ms: 1.11x slower                                                       |
| raytrace                   | 162 ms                                                          | 181 ms: 1.11x slower                                                        |
| xml_etree_process          | 36.4 ms                                                         | 40.6 ms: 1.11x slower                                                       |
| mdp                        | 1.31 sec                                                        | 1.47 sec: 1.12x slower                                                      |
| xml_etree_generate         | 53.2 ms                                                         | 59.7 ms: 1.12x slower                                                       |
| sqlglot_parse              | 748 us                                                          | 840 us: 1.12x slower                                                        |
| asyncio_tcp_ssl            | 1.48 sec                                                        | 1.66 sec: 1.12x slower                                                      |
| coverage                   | 42.1 ms                                                         | 47.2 ms: 1.12x slower                                                       |
| 2to3                       | 207 ms                                                          | 235 ms: 1.13x slower                                                        |
| deltablue                  | 1.88 ms                                                         | 2.14 ms: 1.14x slower                                                       |
| html5lib                   | 35.0 ms                                                         | 40.1 ms: 1.15x slower                                                       |
| hexiom                     | 3.72 ms                                                         | 4.35 ms: 1.17x slower                                                       |
| go                         | 82.1 ms                                                         | 96.6 ms: 1.18x slower                                                       |
| genshi_xml                 | 31.6 ms                                                         | 37.3 ms: 1.18x slower                                                       |
| python_startup             | 20.3 ms                                                         | 23.9 ms: 1.18x slower                                                       |
| mypy2                      | 418 ms                                                          | 501 ms: 1.20x slower                                                        |
| scimark_lu                 | 56.6 ms                                                         | 69.5 ms: 1.23x slower                                                       |
| async_generators           | 223 ms                                                          | 281 ms: 1.26x slower                                                        |
| python_startup_no_site     | 16.2 ms                                                         | 21.6 ms: 1.33x slower                                                       |
| xml_etree_parse            | 90.9 ms                                                         | 123 ms: 1.35x slower                                                        |
| docutils                   | 1.63 sec                                                        | 2.43 sec: 1.49x slower                                                      |
| xml_etree_iterparse        | 62.3 ms                                                         | 94.3 ms: 1.51x slower                                                       |
| float                      | 49.7 ms                                                         | 81.6 ms: 1.64x slower                                                       |
| pylint                     | 205 ms                                                          | 573 ms: 2.80x slower                                                        |
| async_tree_cpu_io_mixed    | 389 ms                                                          | 2.25 sec: 5.79x slower                                                      |
| async_tree_cpu_io_mixed_tg | 382 ms                                                          | 2.46 sec: 6.43x slower                                                      |
| async_tree_none            | 218 ms                                                          | 1.81 sec: 8.31x slower                                                      |
| async_tree_memoization     | 264 ms                                                          | 2.32 sec: 8.78x slower                                                      |
| async_tree_memoization_tg  | 258 ms                                                          | 2.53 sec: 9.79x slower                                                      |
| async_tree_none_tg         | 202 ms                                                          | 1.99 sec: 9.88x slower                                                      |
| async_tree_io              | 588 ms                                                          | 7.30 sec: 12.43x slower                                                     |
| async_tree_io_tg           | 605 ms                                                          | 7.85 sec: 12.97x slower                                                     |
| Geometric mean             | (ref)                                                           | 1.27x slower                                                                |

Benchmark hidden because not significant (3): json_dumps, deepcopy, asyncio_tcp
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240320-3.13.0a5+-dcaf33a-JIT/bm-20240320-pythonperf1-amd64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: unknown