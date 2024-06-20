# Results vs. 3.12.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-amd64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.03x slower
- HPT reliability: 99.92%
- HPT 99th percentile: 1.01x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 232 ms: 1.06x slower                                                        |
| chameleon      | 4.98 ms                                                     | 5.08 ms: 1.02x slower                                                       |
| docutils       | 1.66 sec                                                    | 1.79 sec: 1.08x slower                                                      |
| tornado_http   | 89.5 ms                                                     | 94.8 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                       | 1.05x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 282 ms: 1.30x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 392 ms: 1.28x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 227 ms: 1.26x faster                                                        |
| async_tree_none            | 291 ms                                                      | 238 ms: 1.23x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 405 ms: 1.21x faster                                                        |
| async_tree_io              | 731 ms                                                      | 609 ms: 1.20x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 646 ms: 1.19x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 285 ms: 1.19x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.23x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 54.5 ms: 1.04x faster                                                       |
| pidigits       | 152 ms                                                      | 149 ms: 1.02x faster                                                        |
| nbody          | 71.9 ms                                                     | 74.3 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 118 ms: 1.07x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.59 ms: 1.02x faster                                                       |
| regex_compile  | 87.5 ms                                                     | 106 ms: 1.22x slower                                                        |
| regex_v8       | 14.2 ms                                                     | 20.0 ms: 1.40x slower                                                       |
| Geometric mean | (ref)                                                       | 1.12x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 186 us: 1.05x faster                                                        |
| xml_etree_parse      | 93.0 ms                                                     | 93.7 ms: 1.01x slower                                                       |
| json_dumps           | 5.70 ms                                                     | 5.81 ms: 1.02x slower                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 57.3 ms: 1.03x slower                                                       |
| xml_etree_process    | 37.7 ms                                                     | 38.8 ms: 1.03x slower                                                       |
| unpickle_list        | 2.75 us                                                     | 2.85 us: 1.04x slower                                                       |
| xml_etree_iterparse  | 65.2 ms                                                     | 67.8 ms: 1.04x slower                                                       |
| tomli_loads          | 1.37 sec                                                    | 1.43 sec: 1.04x slower                                                      |
| pickle_list          | 2.83 us                                                     | 2.97 us: 1.05x slower                                                       |
| json_loads           | 13.9 us                                                     | 14.6 us: 1.05x slower                                                       |
| unpickle             | 8.18 us                                                     | 8.83 us: 1.08x slower                                                       |
| pickle_dict          | 18.4 us                                                     | 20.2 us: 1.10x slower                                                       |
| unpickle_pure_python | 133 us                                                      | 159 us: 1.19x slower                                                        |
| Geometric mean       | (ref)                                                       | 1.04x slower                                                                |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                     | 16.7 ms: 1.03x slower                                                       |
| python_startup         | 19.5 ms                                                     | 20.5 ms: 1.05x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 6.96 ms: 1.02x faster                                                       |
| django_template | 22.9 ms                                                     | 24.2 ms: 1.06x slower                                                       |
| Geometric mean  | (ref)                                                       | 1.02x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 282 ms: 1.30x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 392 ms: 1.28x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 227 ms: 1.26x faster                                                        |
| async_tree_none            | 291 ms                                                      | 238 ms: 1.23x faster                                                        |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.73 sec: 1.21x faster                                                      |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 405 ms: 1.21x faster                                                        |
| async_tree_io              | 731 ms                                                      | 609 ms: 1.20x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 646 ms: 1.19x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 285 ms: 1.19x faster                                                        |
| coroutines                 | 14.3 ms                                                     | 13.1 ms: 1.09x faster                                                       |
| raytrace                   | 192 ms                                                      | 177 ms: 1.09x faster                                                        |
| regex_dna                  | 126 ms                                                      | 118 ms: 1.07x faster                                                        |
| sqlite_synth               | 1.76 us                                                     | 1.64 us: 1.07x faster                                                       |
| comprehensions             | 14.1 us                                                     | 13.3 us: 1.06x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 186 us: 1.05x faster                                                        |
| logging_silent             | 60.5 ns                                                     | 57.8 ns: 1.05x faster                                                       |
| richards_super             | 32.1 ms                                                     | 30.7 ms: 1.04x faster                                                       |
| float                      | 56.8 ms                                                     | 54.5 ms: 1.04x faster                                                       |
| richards                   | 28.4 ms                                                     | 27.3 ms: 1.04x faster                                                       |
| deepcopy                   | 238 us                                                      | 231 us: 1.03x faster                                                        |
| deepcopy_reduce            | 2.09 us                                                     | 2.04 us: 1.02x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.56 us: 1.02x faster                                                       |
| pidigits                   | 152 ms                                                      | 149 ms: 1.02x faster                                                        |
| bench_mp_pool              | 69.2 ms                                                     | 67.7 ms: 1.02x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.59 ms: 1.02x faster                                                       |
| mako                       | 7.09 ms                                                     | 6.96 ms: 1.02x faster                                                       |
| logging_simple             | 6.28 us                                                     | 6.20 us: 1.01x faster                                                       |
| xml_etree_parse            | 93.0 ms                                                     | 93.7 ms: 1.01x slower                                                       |
| generators                 | 22.5 ms                                                     | 22.7 ms: 1.01x slower                                                       |
| dulwich_log                | 44.3 ms                                                     | 44.9 ms: 1.01x slower                                                       |
| chaos                      | 43.3 ms                                                     | 44.1 ms: 1.02x slower                                                       |
| pprint_safe_repr           | 513 ms                                                      | 523 ms: 1.02x slower                                                        |
| json_dumps                 | 5.70 ms                                                     | 5.81 ms: 1.02x slower                                                       |
| chameleon                  | 4.98 ms                                                     | 5.08 ms: 1.02x slower                                                       |
| meteor_contest             | 74.6 ms                                                     | 76.3 ms: 1.02x slower                                                       |
| pathlib                    | 80.5 ms                                                     | 82.3 ms: 1.02x slower                                                       |
| python_startup_no_site     | 16.2 ms                                                     | 16.7 ms: 1.03x slower                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 57.3 ms: 1.03x slower                                                       |
| pprint_pformat             | 1.05 sec                                                    | 1.07 sec: 1.03x slower                                                      |
| xml_etree_process          | 37.7 ms                                                     | 38.8 ms: 1.03x slower                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 50.0 ms: 1.03x slower                                                       |
| nbody                      | 71.9 ms                                                     | 74.3 ms: 1.03x slower                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 1.06 ms: 1.04x slower                                                       |
| unpickle_list              | 2.75 us                                                     | 2.85 us: 1.04x slower                                                       |
| xml_etree_iterparse        | 65.2 ms                                                     | 67.8 ms: 1.04x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.58 ms: 1.04x slower                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.43 sec: 1.04x slower                                                      |
| sqlglot_normalize          | 187 ms                                                      | 195 ms: 1.04x slower                                                        |
| sympy_sum                  | 91.5 ms                                                     | 95.6 ms: 1.05x slower                                                       |
| async_generators           | 239 ms                                                      | 251 ms: 1.05x slower                                                        |
| coverage                   | 40.8 ms                                                     | 42.8 ms: 1.05x slower                                                       |
| pickle_list                | 2.83 us                                                     | 2.97 us: 1.05x slower                                                       |
| python_startup             | 19.5 ms                                                     | 20.5 ms: 1.05x slower                                                       |
| json_loads                 | 13.9 us                                                     | 14.6 us: 1.05x slower                                                       |
| django_template            | 22.9 ms                                                     | 24.2 ms: 1.06x slower                                                       |
| tornado_http               | 89.5 ms                                                     | 94.8 ms: 1.06x slower                                                       |
| sympy_str                  | 175 ms                                                      | 185 ms: 1.06x slower                                                        |
| 2to3                       | 218 ms                                                      | 232 ms: 1.06x slower                                                        |
| docutils                   | 1.66 sec                                                    | 1.79 sec: 1.08x slower                                                      |
| unpickle                   | 8.18 us                                                     | 8.83 us: 1.08x slower                                                       |
| sympy_integrate            | 13.0 ms                                                     | 14.0 ms: 1.08x slower                                                       |
| sqlglot_parse              | 804 us                                                      | 874 us: 1.09x slower                                                        |
| fannkuch                   | 247 ms                                                      | 268 ms: 1.09x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 37.7 ms: 1.09x slower                                                       |
| sympy_expand               | 284 ms                                                      | 311 ms: 1.09x slower                                                        |
| scimark_fft                | 184 ms                                                      | 202 ms: 1.10x slower                                                        |
| pycparser                  | 699 ms                                                      | 767 ms: 1.10x slower                                                        |
| pyflate                    | 295 ms                                                      | 324 ms: 1.10x slower                                                        |
| mdp                        | 1.37 sec                                                    | 1.51 sec: 1.10x slower                                                      |
| pickle_dict                | 18.4 us                                                     | 20.2 us: 1.10x slower                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 48.7 ms: 1.11x slower                                                       |
| aiohttp                    | 884 us                                                      | 986 us: 1.11x slower                                                        |
| spectral_norm              | 66.9 ms                                                     | 74.6 ms: 1.12x slower                                                       |
| go                         | 91.6 ms                                                     | 102 ms: 1.12x slower                                                        |
| nqueens                    | 62.8 ms                                                     | 70.7 ms: 1.13x slower                                                       |
| deltablue                  | 2.16 ms                                                     | 2.52 ms: 1.17x slower                                                       |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 3.02 ms: 1.18x slower                                                       |
| scimark_sor                | 78.8 ms                                                     | 92.9 ms: 1.18x slower                                                       |
| unpickle_pure_python       | 133 us                                                      | 159 us: 1.19x slower                                                        |
| telco                      | 4.13 ms                                                     | 4.95 ms: 1.20x slower                                                       |
| regex_compile              | 87.5 ms                                                     | 106 ms: 1.22x slower                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 116 us: 1.22x slower                                                        |
| create_gc_cycles           | 752 us                                                      | 929 us: 1.24x slower                                                        |
| hexiom                     | 4.10 ms                                                     | 5.29 ms: 1.29x slower                                                       |
| scimark_lu                 | 58.9 ms                                                     | 80.8 ms: 1.37x slower                                                       |
| asyncio_tcp                | 487 ms                                                      | 676 ms: 1.39x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 20.0 ms: 1.40x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.03x slower                                                                |

Benchmark hidden because not significant (5): mypy2, deepcopy_memo, pickle, bench_thread_pool, json
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240427-3.13.0a6+-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.92% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: unknown