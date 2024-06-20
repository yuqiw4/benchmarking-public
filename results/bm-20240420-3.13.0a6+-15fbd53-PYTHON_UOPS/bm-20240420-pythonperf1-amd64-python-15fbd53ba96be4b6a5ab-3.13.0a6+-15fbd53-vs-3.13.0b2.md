# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 224 ms: 1.08x slower                                                        |
| chameleon      | 4.80 ms                                                         | 5.02 ms: 1.05x slower                                                       |
| docutils       | 1.63 sec                                                        | 1.74 sec: 1.07x slower                                                      |
| html5lib       | 35.0 ms                                                         | 40.5 ms: 1.16x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 84.1 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                           | 1.08x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg          | 605 ms                                                          | 625 ms: 1.03x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 276 ms: 1.04x slower                                                        |
| async_tree_none           | 218 ms                                                          | 228 ms: 1.05x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 275 ms: 1.06x slower                                                        |
| async_tree_none_tg        | 202 ms                                                          | 226 ms: 1.12x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 148 ms: 1.02x faster                                                        |
| float          | 49.7 ms                                                         | 57.9 ms: 1.17x slower                                                       |
| nbody          | 67.6 ms                                                         | 83.1 ms: 1.23x slower                                                       |
| Geometric mean | (ref)                                                           | 1.12x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                          | 121 ms: 1.02x slower                                                        |
| regex_compile  | 78.0 ms                                                         | 103 ms: 1.32x slower                                                        |
| Geometric mean | (ref)                                                           | 1.07x slower                                                                |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| xml_etree_parse      | 90.9 ms                                                         | 90.0 ms: 1.01x faster                                                       |
| json_dumps           | 5.61 ms                                                         | 5.70 ms: 1.02x slower                                                       |
| unpickle             | 8.40 us                                                         | 8.54 us: 1.02x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 18.6 us: 1.02x slower                                                       |
| pickle_pure_python   | 175 us                                                          | 185 us: 1.05x slower                                                        |
| pickle_list          | 2.90 us                                                         | 3.06 us: 1.05x slower                                                       |
| pickle               | 7.11 us                                                         | 7.53 us: 1.06x slower                                                       |
| xml_etree_process    | 36.4 ms                                                         | 38.7 ms: 1.06x slower                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 56.5 ms: 1.06x slower                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 66.5 ms: 1.07x slower                                                       |
| tomli_loads          | 1.35 sec                                                        | 1.46 sec: 1.08x slower                                                      |
| unpickle_list        | 2.62 us                                                         | 2.86 us: 1.09x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 166 us: 1.36x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.06x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup | 20.3 ms                                                         | 19.9 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                           | 1.01x faster                                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 21.7 ms                                                         | 23.3 ms: 1.07x slower                                                       |
| genshi_xml      | 31.6 ms                                                         | 35.8 ms: 1.13x slower                                                       |
| genshi_text     | 14.4 ms                                                         | 16.4 ms: 1.14x slower                                                       |
| mako            | 6.36 ms                                                         | 7.41 ms: 1.17x slower                                                       |
| Geometric mean  | (ref)                                                           | 1.13x slower                                                                |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 75.7 us: 1.33x faster                                                       |
| json_loads                | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| python_startup            | 20.3 ms                                                         | 19.9 ms: 1.02x faster                                                       |
| pidigits                  | 150 ms                                                          | 148 ms: 1.02x faster                                                        |
| xml_etree_parse           | 90.9 ms                                                         | 90.0 ms: 1.01x faster                                                       |
| bench_mp_pool             | 64.8 ms                                                         | 65.2 ms: 1.01x slower                                                       |
| pathlib                   | 75.9 ms                                                         | 76.5 ms: 1.01x slower                                                       |
| create_gc_cycles          | 888 us                                                          | 900 us: 1.01x slower                                                        |
| sqlite_synth              | 1.60 us                                                         | 1.62 us: 1.01x slower                                                       |
| json_dumps                | 5.61 ms                                                         | 5.70 ms: 1.02x slower                                                       |
| regex_dna                 | 119 ms                                                          | 121 ms: 1.02x slower                                                        |
| unpickle                  | 8.40 us                                                         | 8.54 us: 1.02x slower                                                       |
| aiohttp                   | 889 us                                                          | 907 us: 1.02x slower                                                        |
| coroutines                | 12.8 ms                                                         | 13.0 ms: 1.02x slower                                                       |
| deepcopy_reduce           | 1.99 us                                                         | 2.04 us: 1.02x slower                                                       |
| pickle_dict               | 18.1 us                                                         | 18.6 us: 1.02x slower                                                       |
| tornado_http              | 81.8 ms                                                         | 84.1 ms: 1.03x slower                                                       |
| async_tree_io_tg          | 605 ms                                                          | 625 ms: 1.03x slower                                                        |
| logging_format            | 6.22 us                                                         | 6.45 us: 1.04x slower                                                       |
| deepcopy                  | 220 us                                                          | 229 us: 1.04x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 276 ms: 1.04x slower                                                        |
| chameleon                 | 4.80 ms                                                         | 5.02 ms: 1.05x slower                                                       |
| logging_simple            | 5.78 us                                                         | 6.06 us: 1.05x slower                                                       |
| async_tree_none           | 218 ms                                                          | 228 ms: 1.05x slower                                                        |
| pickle_pure_python        | 175 us                                                          | 185 us: 1.05x slower                                                        |
| pickle_list               | 2.90 us                                                         | 3.06 us: 1.05x slower                                                       |
| generators                | 19.6 ms                                                         | 20.7 ms: 1.06x slower                                                       |
| pickle                    | 7.11 us                                                         | 7.53 us: 1.06x slower                                                       |
| xml_etree_process         | 36.4 ms                                                         | 38.7 ms: 1.06x slower                                                       |
| xml_etree_generate        | 53.2 ms                                                         | 56.5 ms: 1.06x slower                                                       |
| async_tree_memoization_tg | 258 ms                                                          | 275 ms: 1.06x slower                                                        |
| xml_etree_iterparse       | 62.3 ms                                                         | 66.5 ms: 1.07x slower                                                       |
| pylint                    | 205 ms                                                          | 219 ms: 1.07x slower                                                        |
| richards                  | 26.7 ms                                                         | 28.6 ms: 1.07x slower                                                       |
| telco                     | 4.67 ms                                                         | 5.00 ms: 1.07x slower                                                       |
| docutils                  | 1.63 sec                                                        | 1.74 sec: 1.07x slower                                                      |
| django_template           | 21.7 ms                                                         | 23.3 ms: 1.07x slower                                                       |
| richards_super            | 30.2 ms                                                         | 32.4 ms: 1.08x slower                                                       |
| logging_silent            | 52.9 ns                                                         | 57.1 ns: 1.08x slower                                                       |
| tomli_loads               | 1.35 sec                                                        | 1.46 sec: 1.08x slower                                                      |
| sqlglot_normalize         | 173 ms                                                          | 187 ms: 1.08x slower                                                        |
| 2to3                      | 207 ms                                                          | 224 ms: 1.08x slower                                                        |
| raytrace                  | 162 ms                                                          | 176 ms: 1.09x slower                                                        |
| bench_thread_pool         | 768 us                                                          | 835 us: 1.09x slower                                                        |
| async_generators          | 223 ms                                                          | 243 ms: 1.09x slower                                                        |
| unpickle_list             | 2.62 us                                                         | 2.86 us: 1.09x slower                                                       |
| mypy2                     | 418 ms                                                          | 457 ms: 1.09x slower                                                        |
| sqlglot_transpile         | 955 us                                                          | 1.04 ms: 1.09x slower                                                       |
| meteor_contest            | 69.9 ms                                                         | 76.4 ms: 1.09x slower                                                       |
| sqlglot_parse             | 748 us                                                          | 827 us: 1.10x slower                                                        |
| crypto_pyaes              | 45.5 ms                                                         | 50.5 ms: 1.11x slower                                                       |
| async_tree_none_tg        | 202 ms                                                          | 226 ms: 1.12x slower                                                        |
| sqlglot_optimize          | 32.7 ms                                                         | 36.6 ms: 1.12x slower                                                       |
| deepcopy_memo             | 22.1 us                                                         | 24.8 us: 1.12x slower                                                       |
| sympy_sum                 | 84.4 ms                                                         | 94.7 ms: 1.12x slower                                                       |
| sympy_expand              | 271 ms                                                          | 304 ms: 1.12x slower                                                        |
| sympy_integrate           | 12.2 ms                                                         | 13.8 ms: 1.13x slower                                                       |
| thrift                    | 8.11 ms                                                         | 9.18 ms: 1.13x slower                                                       |
| genshi_xml                | 31.6 ms                                                         | 35.8 ms: 1.13x slower                                                       |
| mdp                       | 1.31 sec                                                        | 1.49 sec: 1.13x slower                                                      |
| sympy_str                 | 159 ms                                                          | 181 ms: 1.14x slower                                                        |
| dulwich_log               | 38.0 ms                                                         | 43.4 ms: 1.14x slower                                                       |
| genshi_text               | 14.4 ms                                                         | 16.4 ms: 1.14x slower                                                       |
| pprint_safe_repr          | 474 ms                                                          | 542 ms: 1.14x slower                                                        |
| pprint_pformat            | 966 ms                                                          | 1.11 sec: 1.15x slower                                                      |
| html5lib                  | 35.0 ms                                                         | 40.5 ms: 1.16x slower                                                       |
| chaos                     | 38.4 ms                                                         | 44.6 ms: 1.16x slower                                                       |
| float                     | 49.7 ms                                                         | 57.9 ms: 1.17x slower                                                       |
| mako                      | 6.36 ms                                                         | 7.41 ms: 1.17x slower                                                       |
| coverage                  | 42.1 ms                                                         | 49.1 ms: 1.17x slower                                                       |
| fannkuch                  | 243 ms                                                          | 285 ms: 1.17x slower                                                        |
| pyflate                   | 279 ms                                                          | 336 ms: 1.21x slower                                                        |
| scimark_sor               | 75.3 ms                                                         | 91.1 ms: 1.21x slower                                                       |
| nqueens                   | 56.7 ms                                                         | 68.6 ms: 1.21x slower                                                       |
| scimark_fft               | 171 ms                                                          | 208 ms: 1.22x slower                                                        |
| nbody                     | 67.6 ms                                                         | 83.1 ms: 1.23x slower                                                       |
| go                        | 82.1 ms                                                         | 102 ms: 1.24x slower                                                        |
| spectral_norm             | 63.7 ms                                                         | 81.7 ms: 1.28x slower                                                       |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 3.30 ms: 1.32x slower                                                       |
| scimark_monte_carlo       | 39.1 ms                                                         | 51.6 ms: 1.32x slower                                                       |
| regex_compile             | 78.0 ms                                                         | 103 ms: 1.32x slower                                                        |
| deltablue                 | 1.88 ms                                                         | 2.49 ms: 1.32x slower                                                       |
| comprehensions            | 10.4 us                                                         | 13.8 us: 1.33x slower                                                       |
| unpickle_pure_python      | 122 us                                                          | 166 us: 1.36x slower                                                        |
| scimark_lu                | 56.6 ms                                                         | 78.3 ms: 1.38x slower                                                       |
| hexiom                    | 3.72 ms                                                         | 5.24 ms: 1.41x slower                                                       |
| Geometric mean            | (ref)                                                           | 1.09x slower                                                                |

Benchmark hidden because not significant (11): regex_v8, json, pycparser, gc_traversal, regex_effbot, python_startup_no_site, async_tree_cpu_io_mixed_tg, asyncio_tcp_ssl, async_tree_io, asyncio_tcp, async_tree_cpu_io_mixed
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: unknown