# Results vs. 3.12.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-amd64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 208 ms: 1.05x faster                                                        |
| chameleon      | 4.98 ms                                                     | 4.72 ms: 1.06x faster                                                       |
| docutils       | 1.66 sec                                                    | 1.61 sec: 1.03x faster                                                      |
| tornado_http   | 89.5 ms                                                     | 83.7 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 205 ms: 1.39x faster                                                        |
| async_tree_memoization_tg  | 367 ms                                                      | 270 ms: 1.36x faster                                                        |
| async_tree_none            | 291 ms                                                      | 218 ms: 1.33x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 380 ms: 1.29x faster                                                        |
| async_tree_io              | 731 ms                                                      | 578 ms: 1.26x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 270 ms: 1.25x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 616 ms: 1.25x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.31x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 50.4 ms: 1.13x faster                                                       |
| nbody          | 71.9 ms                                                     | 68.1 ms: 1.06x faster                                                       |
| pidigits       | 152 ms                                                      | 146 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 87.5 ms                                                     | 75.2 ms: 1.16x faster                                                       |
| regex_dna      | 126 ms                                                      | 120 ms: 1.06x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.58 ms: 1.02x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 14.7 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 175 us: 1.12x faster                                                        |
| pickle               | 7.43 us                                                     | 6.96 us: 1.07x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 52.3 ms: 1.07x faster                                                       |
| unpickle_pure_python | 133 us                                                      | 127 us: 1.05x faster                                                        |
| unpickle_list        | 2.75 us                                                     | 2.63 us: 1.05x faster                                                       |
| xml_etree_iterparse  | 65.2 ms                                                     | 62.3 ms: 1.05x faster                                                       |
| xml_etree_process    | 37.7 ms                                                     | 36.5 ms: 1.03x faster                                                       |
| json_dumps           | 5.70 ms                                                     | 5.58 ms: 1.02x faster                                                       |
| pickle_dict          | 18.4 us                                                     | 18.0 us: 1.02x faster                                                       |
| xml_etree_parse      | 93.0 ms                                                     | 91.2 ms: 1.02x faster                                                       |
| json_loads           | 13.9 us                                                     | 13.8 us: 1.01x faster                                                       |
| pickle_list          | 2.83 us                                                     | 2.84 us: 1.01x slower                                                       |
| unpickle             | 8.18 us                                                     | 8.38 us: 1.02x slower                                                       |
| tomli_loads          | 1.37 sec                                                    | 1.41 sec: 1.03x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 20.0 ms: 1.03x slower                                                       |
| python_startup_no_site | 16.2 ms                                                     | 18.5 ms: 1.14x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 6.26 ms: 1.13x faster                                                       |
| django_template | 22.9 ms                                                     | 21.8 ms: 1.05x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.09x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 205 ms: 1.39x faster                                                        |
| async_tree_memoization_tg  | 367 ms                                                      | 270 ms: 1.36x faster                                                        |
| comprehensions             | 14.1 us                                                     | 10.4 us: 1.36x faster                                                       |
| async_tree_none            | 291 ms                                                      | 218 ms: 1.33x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 72.1 us: 1.32x faster                                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 380 ms: 1.29x faster                                                        |
| async_tree_io              | 731 ms                                                      | 578 ms: 1.26x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 270 ms: 1.25x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 616 ms: 1.25x faster                                                        |
| raytrace                   | 192 ms                                                      | 159 ms: 1.21x faster                                                        |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.75 sec: 1.20x faster                                                      |
| mypy2                      | 509 ms                                                      | 433 ms: 1.18x faster                                                        |
| chaos                      | 43.3 ms                                                     | 37.1 ms: 1.17x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 75.2 ms: 1.16x faster                                                       |
| scimark_lu                 | 58.9 ms                                                     | 50.8 ms: 1.16x faster                                                       |
| spectral_norm              | 66.9 ms                                                     | 58.4 ms: 1.15x faster                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 38.6 ms: 1.13x faster                                                       |
| mako                       | 7.09 ms                                                     | 6.26 ms: 1.13x faster                                                       |
| float                      | 56.8 ms                                                     | 50.4 ms: 1.13x faster                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 43.1 ms: 1.12x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 175 us: 1.12x faster                                                        |
| hexiom                     | 4.10 ms                                                     | 3.67 ms: 1.12x faster                                                       |
| scimark_fft                | 184 ms                                                      | 165 ms: 1.12x faster                                                        |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.29 ms: 1.11x faster                                                       |
| deepcopy_memo              | 23.7 us                                                     | 21.3 us: 1.11x faster                                                       |
| dulwich_log                | 44.3 ms                                                     | 40.0 ms: 1.11x faster                                                       |
| sympy_str                  | 175 ms                                                      | 158 ms: 1.11x faster                                                        |
| sqlite_synth               | 1.76 us                                                     | 1.59 us: 1.11x faster                                                       |
| sympy_sum                  | 91.5 ms                                                     | 82.9 ms: 1.10x faster                                                       |
| deepcopy                   | 238 us                                                      | 216 us: 1.10x faster                                                        |
| logging_silent             | 60.5 ns                                                     | 55.1 ns: 1.10x faster                                                       |
| nqueens                    | 62.8 ms                                                     | 57.3 ms: 1.10x faster                                                       |
| go                         | 91.6 ms                                                     | 83.6 ms: 1.09x faster                                                       |
| deltablue                  | 2.16 ms                                                     | 1.98 ms: 1.09x faster                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 63.8 ms: 1.08x faster                                                       |
| scimark_sor                | 78.8 ms                                                     | 72.7 ms: 1.08x faster                                                       |
| deepcopy_reduce            | 2.09 us                                                     | 1.94 us: 1.08x faster                                                       |
| sqlglot_parse              | 804 us                                                      | 745 us: 1.08x faster                                                        |
| pprint_pformat             | 1.05 sec                                                    | 970 ms: 1.08x faster                                                        |
| pprint_safe_repr           | 513 ms                                                      | 476 ms: 1.08x faster                                                        |
| richards_super             | 32.1 ms                                                     | 30.0 ms: 1.07x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 83.7 ms: 1.07x faster                                                       |
| pickle                     | 7.43 us                                                     | 6.96 us: 1.07x faster                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 52.3 ms: 1.07x faster                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 958 us: 1.07x faster                                                        |
| richards                   | 28.4 ms                                                     | 26.6 ms: 1.07x faster                                                       |
| sqlglot_normalize          | 187 ms                                                      | 175 ms: 1.07x faster                                                        |
| sympy_integrate            | 13.0 ms                                                     | 12.2 ms: 1.06x faster                                                       |
| meteor_contest             | 74.6 ms                                                     | 70.5 ms: 1.06x faster                                                       |
| nbody                      | 71.9 ms                                                     | 68.1 ms: 1.06x faster                                                       |
| regex_dna                  | 126 ms                                                      | 120 ms: 1.06x faster                                                        |
| chameleon                  | 4.98 ms                                                     | 4.72 ms: 1.06x faster                                                       |
| logging_simple             | 6.28 us                                                     | 5.95 us: 1.06x faster                                                       |
| bench_thread_pool          | 857 us                                                      | 814 us: 1.05x faster                                                        |
| django_template            | 22.9 ms                                                     | 21.8 ms: 1.05x faster                                                       |
| pyflate                    | 295 ms                                                      | 280 ms: 1.05x faster                                                        |
| unpickle_pure_python       | 133 us                                                      | 127 us: 1.05x faster                                                        |
| unpickle_list              | 2.75 us                                                     | 2.63 us: 1.05x faster                                                       |
| xml_etree_iterparse        | 65.2 ms                                                     | 62.3 ms: 1.05x faster                                                       |
| 2to3                       | 218 ms                                                      | 208 ms: 1.05x faster                                                        |
| coroutines                 | 14.3 ms                                                     | 13.7 ms: 1.04x faster                                                       |
| json                       | 3.05 ms                                                     | 2.92 ms: 1.04x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.44 us: 1.04x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 33.1 ms: 1.04x faster                                                       |
| pidigits                   | 152 ms                                                      | 146 ms: 1.04x faster                                                        |
| asyncio_tcp                | 487 ms                                                      | 469 ms: 1.04x faster                                                        |
| pycparser                  | 699 ms                                                      | 675 ms: 1.04x faster                                                        |
| sympy_expand               | 284 ms                                                      | 274 ms: 1.04x faster                                                        |
| xml_etree_process          | 37.7 ms                                                     | 36.5 ms: 1.03x faster                                                       |
| pathlib                    | 80.5 ms                                                     | 78.0 ms: 1.03x faster                                                       |
| docutils                   | 1.66 sec                                                    | 1.61 sec: 1.03x faster                                                      |
| unpack_sequence            | 37.5 ns                                                     | 36.7 ns: 1.02x faster                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.58 ms: 1.02x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.58 ms: 1.02x faster                                                       |
| pickle_dict                | 18.4 us                                                     | 18.0 us: 1.02x faster                                                       |
| xml_etree_parse            | 93.0 ms                                                     | 91.2 ms: 1.02x faster                                                       |
| fannkuch                   | 247 ms                                                      | 243 ms: 1.02x faster                                                        |
| json_loads                 | 13.9 us                                                     | 13.8 us: 1.01x faster                                                       |
| pickle_list                | 2.83 us                                                     | 2.84 us: 1.01x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.53 ms: 1.01x slower                                                       |
| aiohttp                    | 884 us                                                      | 895 us: 1.01x slower                                                        |
| unpickle                   | 8.18 us                                                     | 8.38 us: 1.02x slower                                                       |
| python_startup             | 19.5 ms                                                     | 20.0 ms: 1.03x slower                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.41 sec: 1.03x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 14.7 ms: 1.03x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 847 us: 1.13x slower                                                        |
| coverage                   | 40.8 ms                                                     | 46.3 ms: 1.13x slower                                                       |
| python_startup_no_site     | 16.2 ms                                                     | 18.5 ms: 1.14x slower                                                       |
| telco                      | 4.13 ms                                                     | 4.77 ms: 1.15x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                                |

Benchmark hidden because not significant (3): async_generators, mdp, generators
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: unknown