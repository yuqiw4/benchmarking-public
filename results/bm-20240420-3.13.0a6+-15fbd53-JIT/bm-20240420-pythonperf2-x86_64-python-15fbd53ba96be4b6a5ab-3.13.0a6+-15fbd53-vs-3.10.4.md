# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.27x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 298 ms: 1.18x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.57 ms: 1.25x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.05 sec: 1.12x faster                                                       |
| html5lib       | 94.6 ms                                                      | 74.6 ms: 1.27x faster                                                        |
| tornado_http   | 157 ms                                                       | 122 ms: 1.28x faster                                                         |
| Geometric mean | (ref)                                                        | 1.22x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 372 ms: 1.86x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 903 ms: 1.77x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 467 ms: 1.75x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 617 ms: 1.52x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.72x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 75.6 ms: 1.47x faster                                                        |
| nbody          | 134 ms                                                       | 98.2 ms: 1.37x faster                                                        |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                        | 1.28x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 145 ms: 1.31x faster                                                         |
| regex_dna      | 261 ms                                                       | 241 ms: 1.08x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 26.2 ms: 1.04x faster                                                        |
| regex_effbot   | 3.09 ms                                                      | 3.47 ms: 1.12x slower                                                        |
| Geometric mean | (ref)                                                        | 1.07x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 311 us: 1.46x faster                                                         |
| unpickle_pure_python | 312 us                                                       | 219 us: 1.42x faster                                                         |
| tomli_loads          | 2.92 sec                                                     | 2.14 sec: 1.36x faster                                                       |
| json_dumps           | 14.5 ms                                                      | 10.8 ms: 1.35x faster                                                        |
| xml_etree_process    | 75.9 ms                                                      | 57.6 ms: 1.32x faster                                                        |
| json_loads           | 30.3 us                                                      | 24.8 us: 1.23x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 144 ms: 1.11x faster                                                         |
| xml_etree_generate   | 92.3 ms                                                      | 83.7 ms: 1.10x faster                                                        |
| xml_etree_iterparse  | 110 ms                                                       | 101 ms: 1.09x faster                                                         |
| pickle_list          | 4.12 us                                                      | 4.41 us: 1.07x slower                                                        |
| pickle               | 9.89 us                                                      | 10.8 us: 1.09x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 32.5 us: 1.10x slower                                                        |
| unpickle             | 13.5 us                                                      | 15.3 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.18x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 9.45 ms: 1.29x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.23x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 9.93 ms: 1.48x faster                                                        |
| django_template | 50.2 ms                                                      | 39.4 ms: 1.27x faster                                                        |
| genshi_text     | 31.4 ms                                                      | 26.0 ms: 1.21x faster                                                        |
| genshi_xml      | 63.3 ms                                                      | 58.3 ms: 1.09x faster                                                        |
| Geometric mean  | (ref)                                                        | 1.25x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 121 us: 4.44x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 374 ms: 2.08x faster                                                         |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                                       |
| deltablue                | 7.50 ms                                                      | 3.83 ms: 1.96x faster                                                        |
| async_tree_none          | 692 ms                                                       | 372 ms: 1.86x faster                                                         |
| raytrace                 | 489 ms                                                       | 271 ms: 1.80x faster                                                         |
| async_tree_io            | 1.60 sec                                                     | 903 ms: 1.77x faster                                                         |
| logging_silent           | 167 ns                                                       | 94.7 ns: 1.77x faster                                                        |
| async_tree_memoization   | 819 ms                                                       | 467 ms: 1.75x faster                                                         |
| richards_super           | 90.6 ms                                                      | 52.2 ms: 1.74x faster                                                        |
| generators               | 57.3 ms                                                      | 33.5 ms: 1.71x faster                                                        |
| chaos                    | 109 ms                                                       | 65.6 ms: 1.66x faster                                                        |
| richards                 | 75.1 ms                                                      | 46.2 ms: 1.62x faster                                                        |
| pylint                   | 566 ms                                                       | 362 ms: 1.57x faster                                                         |
| sqlglot_parse            | 2.24 ms                                                      | 1.44 ms: 1.56x faster                                                        |
| crypto_pyaes             | 119 ms                                                       | 77.3 ms: 1.54x faster                                                        |
| pyflate                  | 733 ms                                                       | 483 ms: 1.52x faster                                                         |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 617 ms: 1.52x faster                                                         |
| spectral_norm            | 139 ms                                                       | 92.7 ms: 1.50x faster                                                        |
| mako                     | 14.7 ms                                                      | 9.93 ms: 1.48x faster                                                        |
| scimark_monte_carlo      | 107 ms                                                       | 72.6 ms: 1.48x faster                                                        |
| float                    | 111 ms                                                       | 75.6 ms: 1.47x faster                                                        |
| go                       | 262 ms                                                       | 178 ms: 1.47x faster                                                         |
| pickle_pure_python       | 455 us                                                       | 311 us: 1.46x faster                                                         |
| sqlglot_transpile        | 2.68 ms                                                      | 1.84 ms: 1.46x faster                                                        |
| unpickle_pure_python     | 312 us                                                       | 219 us: 1.42x faster                                                         |
| logging_simple           | 8.88 us                                                      | 6.25 us: 1.42x faster                                                        |
| logging_format           | 9.64 us                                                      | 6.89 us: 1.40x faster                                                        |
| comprehensions           | 26.7 us                                                      | 19.2 us: 1.39x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 4.65 ms: 1.37x faster                                                        |
| coroutines               | 30.3 ms                                                      | 22.1 ms: 1.37x faster                                                        |
| nbody                    | 134 ms                                                       | 98.2 ms: 1.37x faster                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.14 sec: 1.36x faster                                                       |
| pycparser                | 1.67 sec                                                     | 1.23 sec: 1.36x faster                                                       |
| json_dumps               | 14.5 ms                                                      | 10.8 ms: 1.35x faster                                                        |
| deepcopy_memo            | 49.8 us                                                      | 37.3 us: 1.34x faster                                                        |
| scimark_lu               | 167 ms                                                       | 125 ms: 1.33x faster                                                         |
| xml_etree_process        | 75.9 ms                                                      | 57.6 ms: 1.32x faster                                                        |
| thrift                   | 1.18 ms                                                      | 893 us: 1.32x faster                                                         |
| hexiom                   | 9.42 ms                                                      | 7.15 ms: 1.32x faster                                                        |
| regex_compile            | 190 ms                                                       | 145 ms: 1.31x faster                                                         |
| fannkuch                 | 483 ms                                                       | 374 ms: 1.29x faster                                                         |
| tornado_http             | 157 ms                                                       | 122 ms: 1.28x faster                                                         |
| django_template          | 50.2 ms                                                      | 39.4 ms: 1.27x faster                                                        |
| html5lib                 | 94.6 ms                                                      | 74.6 ms: 1.27x faster                                                        |
| pprint_safe_repr         | 1.05 sec                                                     | 831 ms: 1.26x faster                                                         |
| pprint_pformat           | 2.15 sec                                                     | 1.71 sec: 1.26x faster                                                       |
| chameleon                | 9.44 ms                                                      | 7.57 ms: 1.25x faster                                                        |
| bench_thread_pool        | 1.14 ms                                                      | 926 us: 1.23x faster                                                         |
| deepcopy                 | 468 us                                                       | 382 us: 1.23x faster                                                         |
| json_loads               | 30.3 us                                                      | 24.8 us: 1.23x faster                                                        |
| pathlib                  | 21.4 ms                                                      | 17.5 ms: 1.22x faster                                                        |
| dulwich_log              | 81.1 ms                                                      | 66.6 ms: 1.22x faster                                                        |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.20 ms: 1.21x faster                                                        |
| genshi_text              | 31.4 ms                                                      | 26.0 ms: 1.21x faster                                                        |
| sympy_sum                | 193 ms                                                       | 162 ms: 1.19x faster                                                         |
| scimark_sor              | 180 ms                                                       | 152 ms: 1.19x faster                                                         |
| dask                     | 472 ms                                                       | 399 ms: 1.18x faster                                                         |
| deepcopy_reduce          | 4.01 us                                                      | 3.40 us: 1.18x faster                                                        |
| sympy_str                | 360 ms                                                       | 306 ms: 1.18x faster                                                         |
| 2to3                     | 350 ms                                                       | 298 ms: 1.18x faster                                                         |
| sympy_expand             | 600 ms                                                       | 510 ms: 1.18x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 123 ms: 1.17x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.59 sec: 1.16x faster                                                       |
| nqueens                  | 115 ms                                                       | 100 ms: 1.15x faster                                                         |
| scimark_fft              | 361 ms                                                       | 316 ms: 1.15x faster                                                         |
| mypy2                    | 933 ms                                                       | 820 ms: 1.14x faster                                                         |
| sympy_integrate          | 28.2 ms                                                      | 25.0 ms: 1.13x faster                                                        |
| sqlglot_optimize         | 70.1 ms                                                      | 62.6 ms: 1.12x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.05 sec: 1.12x faster                                                       |
| sqlite_synth             | 2.99 us                                                      | 2.68 us: 1.11x faster                                                        |
| xml_etree_parse          | 160 ms                                                       | 144 ms: 1.11x faster                                                         |
| xml_etree_generate       | 92.3 ms                                                      | 83.7 ms: 1.10x faster                                                        |
| json                     | 5.86 ms                                                      | 5.35 ms: 1.10x faster                                                        |
| xml_etree_iterparse      | 110 ms                                                       | 101 ms: 1.09x faster                                                         |
| genshi_xml               | 63.3 ms                                                      | 58.3 ms: 1.09x faster                                                        |
| regex_dna                | 261 ms                                                       | 241 ms: 1.08x faster                                                         |
| async_generators         | 421 ms                                                       | 388 ms: 1.08x faster                                                         |
| gunicorn                 | 1.16 ms                                                      | 1.10 ms: 1.06x faster                                                        |
| aiohttp                  | 1.19 ms                                                      | 1.13 ms: 1.06x faster                                                        |
| meteor_contest           | 138 ms                                                       | 131 ms: 1.05x faster                                                         |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| regex_v8                 | 27.2 ms                                                      | 26.2 ms: 1.04x faster                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.88 ms: 1.07x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.41 us: 1.07x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.8 us: 1.09x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 32.5 us: 1.10x slower                                                        |
| telco                    | 7.23 ms                                                      | 8.06 ms: 1.11x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.47 ms: 1.12x slower                                                        |
| unpickle                 | 13.5 us                                                      | 15.3 us: 1.13x slower                                                        |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.18x slower                                                        |
| coverage                 | 63.3 ms                                                      | 79.5 ms: 1.26x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.40 ms: 1.29x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 9.45 ms: 1.29x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.27x faster                                                                 |

Benchmark hidden because not significant (2): unpickle_list, asyncio_websockets
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: 1.20x