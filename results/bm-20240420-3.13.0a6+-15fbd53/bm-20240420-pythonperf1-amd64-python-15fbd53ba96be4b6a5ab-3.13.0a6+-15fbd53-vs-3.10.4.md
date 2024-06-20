# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 211 ms: 1.16x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.91 ms: 1.18x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.64 sec: 1.17x faster                                                      |
| html5lib       | 51.0 ms                                                     | 36.3 ms: 1.41x faster                                                       |
| tornado_http   | 108 ms                                                      | 81.8 ms: 1.32x faster                                                       |
| Geometric mean | (ref)                                                       | 1.25x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 227 ms: 1.92x faster                                                        |
| async_tree_memoization  | 526 ms                                                      | 275 ms: 1.91x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 592 ms: 1.87x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 398 ms: 1.60x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.82x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 53.0 ms: 1.17x faster                                                       |
| pidigits       | 149 ms                                                      | 148 ms: 1.01x faster                                                        |
| nbody          | 71.3 ms                                                     | 72.4 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 79.7 ms: 1.33x faster                                                       |
| regex_dna      | 136 ms                                                      | 125 ms: 1.09x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.60 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                       | 1.11x faster                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.76 ms: 1.59x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 183 us: 1.47x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 135 us: 1.35x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.42 sec: 1.18x faster                                                      |
| xml_etree_process    | 44.5 ms                                                     | 38.2 ms: 1.16x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.54 us: 1.06x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 92.9 ms: 1.04x faster                                                       |
| json_loads           | 14.0 us                                                     | 13.7 us: 1.03x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 56.2 ms: 1.01x slower                                                       |
| pickle               | 6.85 us                                                     | 7.20 us: 1.05x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.4 us: 1.07x slower                                                       |
| pickle_list          | 2.75 us                                                     | 3.22 us: 1.17x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.10x faster                                                                |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 20.4 ms: 1.01x faster                                                       |
| python_startup_no_site | 15.5 ms                                                     | 16.9 ms: 1.09x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 6.46 ms: 1.40x faster                                                       |
| django_template | 28.9 ms                                                     | 22.4 ms: 1.29x faster                                                       |
| genshi_text     | 19.8 ms                                                     | 16.5 ms: 1.20x faster                                                       |
| genshi_xml      | 41.0 ms                                                     | 35.0 ms: 1.17x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.26x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 74.9 us: 4.49x faster                                                       |
| deltablue                | 4.19 ms                                                     | 2.10 ms: 1.99x faster                                                       |
| async_tree_none          | 435 ms                                                      | 227 ms: 1.92x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 275 ms: 1.91x faster                                                        |
| async_tree_io            | 1.11 sec                                                    | 592 ms: 1.87x faster                                                        |
| pylint                   | 350 ms                                                      | 208 ms: 1.68x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 57.4 ns: 1.65x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 398 ms: 1.60x faster                                                        |
| json_dumps               | 9.16 ms                                                     | 5.76 ms: 1.59x faster                                                       |
| raytrace                 | 273 ms                                                      | 172 ms: 1.59x faster                                                        |
| richards_super           | 52.2 ms                                                     | 33.2 ms: 1.57x faster                                                       |
| generators               | 32.4 ms                                                     | 20.7 ms: 1.57x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 781 us: 1.56x faster                                                        |
| chaos                    | 61.7 ms                                                     | 39.8 ms: 1.55x faster                                                       |
| asyncio_tcp              | 732 ms                                                      | 474 ms: 1.55x faster                                                        |
| go                       | 139 ms                                                      | 91.4 ms: 1.52x faster                                                       |
| scimark_lu               | 85.8 ms                                                     | 56.9 ms: 1.51x faster                                                       |
| sqlglot_transpile        | 1.48 ms                                                     | 988 us: 1.49x faster                                                        |
| comprehensions           | 16.5 us                                                     | 11.1 us: 1.48x faster                                                       |
| pickle_pure_python       | 270 us                                                      | 183 us: 1.47x faster                                                        |
| richards                 | 42.4 ms                                                     | 29.5 ms: 1.44x faster                                                       |
| hexiom                   | 5.74 ms                                                     | 3.99 ms: 1.44x faster                                                       |
| html5lib                 | 51.0 ms                                                     | 36.3 ms: 1.41x faster                                                       |
| mako                     | 9.03 ms                                                     | 6.46 ms: 1.40x faster                                                       |
| pyflate                  | 409 ms                                                      | 293 ms: 1.40x faster                                                        |
| crypto_pyaes             | 62.5 ms                                                     | 45.7 ms: 1.37x faster                                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 42.1 ms: 1.36x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 135 us: 1.35x faster                                                        |
| scimark_sor              | 106 ms                                                      | 79.1 ms: 1.34x faster                                                       |
| mypy2                    | 555 ms                                                      | 415 ms: 1.34x faster                                                        |
| regex_compile            | 106 ms                                                      | 79.7 ms: 1.33x faster                                                       |
| tornado_http             | 108 ms                                                      | 81.8 ms: 1.32x faster                                                       |
| mdp                      | 1.78 sec                                                    | 1.36 sec: 1.31x faster                                                      |
| django_template          | 28.9 ms                                                     | 22.4 ms: 1.29x faster                                                       |
| dulwich_log              | 50.5 ms                                                     | 39.7 ms: 1.27x faster                                                       |
| sympy_sum                | 107 ms                                                      | 85.0 ms: 1.26x faster                                                       |
| deepcopy_memo            | 28.8 us                                                     | 23.1 us: 1.24x faster                                                       |
| pycparser                | 930 ms                                                      | 754 ms: 1.23x faster                                                        |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.72 sec: 1.23x faster                                                      |
| sympy_integrate          | 15.3 ms                                                     | 12.6 ms: 1.21x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 1.01 sec: 1.21x faster                                                      |
| spectral_norm            | 77.3 ms                                                     | 64.2 ms: 1.20x faster                                                       |
| genshi_text              | 19.8 ms                                                     | 16.5 ms: 1.20x faster                                                       |
| sympy_str                | 194 ms                                                      | 162 ms: 1.20x faster                                                        |
| pprint_safe_repr         | 592 ms                                                      | 494 ms: 1.20x faster                                                        |
| sqlite_synth             | 1.91 us                                                     | 1.61 us: 1.18x faster                                                       |
| sqlglot_optimize         | 39.8 ms                                                     | 33.6 ms: 1.18x faster                                                       |
| coroutines               | 16.0 ms                                                     | 13.6 ms: 1.18x faster                                                       |
| tomli_loads              | 1.67 sec                                                    | 1.42 sec: 1.18x faster                                                      |
| chameleon                | 5.79 ms                                                     | 4.91 ms: 1.18x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 815 us: 1.17x faster                                                        |
| docutils                 | 1.92 sec                                                    | 1.64 sec: 1.17x faster                                                      |
| genshi_xml               | 41.0 ms                                                     | 35.0 ms: 1.17x faster                                                       |
| float                    | 61.7 ms                                                     | 53.0 ms: 1.17x faster                                                       |
| xml_etree_process        | 44.5 ms                                                     | 38.2 ms: 1.16x faster                                                       |
| 2to3                     | 246 ms                                                      | 211 ms: 1.16x faster                                                        |
| sqlglot_normalize        | 205 ms                                                      | 178 ms: 1.15x faster                                                        |
| sympy_expand             | 314 ms                                                      | 275 ms: 1.14x faster                                                        |
| deepcopy                 | 255 us                                                      | 226 us: 1.13x faster                                                        |
| nqueens                  | 66.6 ms                                                     | 59.2 ms: 1.13x faster                                                       |
| aiohttp                  | 995 us                                                      | 889 us: 1.12x faster                                                        |
| regex_dna                | 136 ms                                                      | 125 ms: 1.09x faster                                                        |
| json                     | 3.14 ms                                                     | 2.87 ms: 1.09x faster                                                       |
| deepcopy_reduce          | 2.20 us                                                     | 2.03 us: 1.08x faster                                                       |
| unpickle                 | 9.09 us                                                     | 8.54 us: 1.06x faster                                                       |
| logging_format           | 6.76 us                                                     | 6.47 us: 1.04x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 92.9 ms: 1.04x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.60 ms: 1.03x faster                                                       |
| logging_simple           | 6.22 us                                                     | 6.03 us: 1.03x faster                                                       |
| json_loads               | 14.0 us                                                     | 13.7 us: 1.03x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 74.3 ms: 1.02x faster                                                       |
| scimark_fft              | 187 ms                                                      | 185 ms: 1.01x faster                                                        |
| python_startup           | 20.6 ms                                                     | 20.4 ms: 1.01x faster                                                       |
| pidigits                 | 149 ms                                                      | 148 ms: 1.01x faster                                                        |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.70 ms: 1.01x faster                                                       |
| fannkuch                 | 256 ms                                                      | 259 ms: 1.01x slower                                                        |
| xml_etree_generate       | 55.5 ms                                                     | 56.2 ms: 1.01x slower                                                       |
| nbody                    | 71.3 ms                                                     | 72.4 ms: 1.02x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 64.3 ms: 1.04x slower                                                       |
| async_generators         | 222 ms                                                      | 231 ms: 1.04x slower                                                        |
| pickle                   | 6.85 us                                                     | 7.20 us: 1.05x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 18.4 us: 1.07x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 16.9 ms: 1.09x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.54 ms: 1.09x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 901 us: 1.13x slower                                                        |
| pickle_list              | 2.75 us                                                     | 3.22 us: 1.17x slower                                                       |
| coverage                 | 39.0 ms                                                     | 45.8 ms: 1.17x slower                                                       |
| telco                    | 3.94 ms                                                     | 5.00 ms: 1.27x slower                                                       |
| thrift                   | 617 us                                                      | 8.13 ms: 13.17x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.20x faster                                                                |

Benchmark hidden because not significant (4): pathlib, regex_v8, xml_etree_iterparse, unpickle_list
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown