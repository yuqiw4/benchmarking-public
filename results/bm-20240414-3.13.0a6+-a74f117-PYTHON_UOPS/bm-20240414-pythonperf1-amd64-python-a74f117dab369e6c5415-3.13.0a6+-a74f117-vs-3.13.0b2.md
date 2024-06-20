# Results vs. 3.13.0b2

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 222 ms: 1.07x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.90 ms: 1.02x slower                                                       |
| docutils       | 1.63 sec                                                        | 1.75 sec: 1.08x slower                                                      |
| html5lib       | 35.0 ms                                                         | 36.9 ms: 1.05x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 83.9 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                           | 1.05x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg          | 605 ms                                                          | 621 ms: 1.03x slower                                                        |
| async_tree_none           | 218 ms                                                          | 226 ms: 1.04x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 275 ms: 1.04x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 273 ms: 1.06x slower                                                        |
| async_tree_none_tg        | 202 ms                                                          | 220 ms: 1.09x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.03x slower                                                                |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| float          | 49.7 ms                                                         | 57.0 ms: 1.15x slower                                                       |
| nbody          | 67.6 ms                                                         | 79.3 ms: 1.17x slower                                                       |
| Geometric mean | (ref)                                                           | 1.10x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                         | 1.59 ms: 1.00x slower                                                       |
| regex_dna      | 119 ms                                                          | 121 ms: 1.02x slower                                                        |
| regex_compile  | 78.0 ms                                                         | 103 ms: 1.32x slower                                                        |
| Geometric mean | (ref)                                                           | 1.07x slower                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_list          | 2.90 us                                                         | 2.82 us: 1.03x faster                                                       |
| json_loads           | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| json_dumps           | 5.61 ms                                                         | 5.66 ms: 1.01x slower                                                       |
| pickle               | 7.11 us                                                         | 7.17 us: 1.01x slower                                                       |
| xml_etree_parse      | 90.9 ms                                                         | 92.1 ms: 1.01x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 18.7 us: 1.03x slower                                                       |
| pickle_pure_python   | 175 us                                                          | 182 us: 1.04x slower                                                        |
| unpickle             | 8.40 us                                                         | 8.83 us: 1.05x slower                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 66.6 ms: 1.07x slower                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 56.9 ms: 1.07x slower                                                       |
| xml_etree_process    | 36.4 ms                                                         | 39.1 ms: 1.07x slower                                                       |
| tomli_loads          | 1.35 sec                                                        | 1.46 sec: 1.08x slower                                                      |
| unpickle_list        | 2.62 us                                                         | 2.88 us: 1.10x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 155 us: 1.27x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.05x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup | 20.3 ms                                                         | 19.7 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 6.36 ms                                                         | 7.07 ms: 1.11x slower                                                       |
| genshi_xml     | 31.6 ms                                                         | 35.8 ms: 1.13x slower                                                       |
| genshi_text    | 14.4 ms                                                         | 16.7 ms: 1.16x slower                                                       |
| Geometric mean | (ref)                                                           | 1.14x slower                                                                |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 76.6 us: 1.32x faster                                                       |
| json                      | 3.19 ms                                                         | 2.96 ms: 1.08x faster                                                       |
| python_startup            | 20.3 ms                                                         | 19.7 ms: 1.03x faster                                                       |
| pickle_list               | 2.90 us                                                         | 2.82 us: 1.03x faster                                                       |
| json_loads                | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| pidigits                  | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| regex_effbot              | 1.58 ms                                                         | 1.59 ms: 1.00x slower                                                       |
| bench_mp_pool             | 64.8 ms                                                         | 65.2 ms: 1.01x slower                                                       |
| deepcopy_reduce           | 1.99 us                                                         | 2.01 us: 1.01x slower                                                       |
| json_dumps                | 5.61 ms                                                         | 5.66 ms: 1.01x slower                                                       |
| pickle                    | 7.11 us                                                         | 7.17 us: 1.01x slower                                                       |
| xml_etree_parse           | 90.9 ms                                                         | 92.1 ms: 1.01x slower                                                       |
| regex_dna                 | 119 ms                                                          | 121 ms: 1.02x slower                                                        |
| chameleon                 | 4.80 ms                                                         | 4.90 ms: 1.02x slower                                                       |
| richards                  | 26.7 ms                                                         | 27.3 ms: 1.02x slower                                                       |
| create_gc_cycles          | 888 us                                                          | 909 us: 1.02x slower                                                        |
| aiohttp                   | 889 us                                                          | 911 us: 1.03x slower                                                        |
| tornado_http              | 81.8 ms                                                         | 83.9 ms: 1.03x slower                                                       |
| async_tree_io_tg          | 605 ms                                                          | 621 ms: 1.03x slower                                                        |
| pickle_dict               | 18.1 us                                                         | 18.7 us: 1.03x slower                                                       |
| sqlite_synth              | 1.60 us                                                         | 1.65 us: 1.03x slower                                                       |
| coroutines                | 12.8 ms                                                         | 13.2 ms: 1.04x slower                                                       |
| async_tree_none           | 218 ms                                                          | 226 ms: 1.04x slower                                                        |
| richards_super            | 30.2 ms                                                         | 31.2 ms: 1.04x slower                                                       |
| pickle_pure_python        | 175 us                                                          | 182 us: 1.04x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 275 ms: 1.04x slower                                                        |
| unpickle                  | 8.40 us                                                         | 8.83 us: 1.05x slower                                                       |
| deepcopy                  | 220 us                                                          | 231 us: 1.05x slower                                                        |
| html5lib                  | 35.0 ms                                                         | 36.9 ms: 1.05x slower                                                       |
| async_tree_memoization_tg | 258 ms                                                          | 273 ms: 1.06x slower                                                        |
| logging_simple            | 5.78 us                                                         | 6.14 us: 1.06x slower                                                       |
| logging_format            | 6.22 us                                                         | 6.62 us: 1.06x slower                                                       |
| deepcopy_memo             | 22.1 us                                                         | 23.5 us: 1.07x slower                                                       |
| xml_etree_iterparse       | 62.3 ms                                                         | 66.6 ms: 1.07x slower                                                       |
| xml_etree_generate        | 53.2 ms                                                         | 56.9 ms: 1.07x slower                                                       |
| meteor_contest            | 69.9 ms                                                         | 74.9 ms: 1.07x slower                                                       |
| 2to3                      | 207 ms                                                          | 222 ms: 1.07x slower                                                        |
| xml_etree_process         | 36.4 ms                                                         | 39.1 ms: 1.07x slower                                                       |
| logging_silent            | 52.9 ns                                                         | 56.8 ns: 1.07x slower                                                       |
| telco                     | 4.67 ms                                                         | 5.03 ms: 1.08x slower                                                       |
| bench_thread_pool         | 768 us                                                          | 827 us: 1.08x slower                                                        |
| raytrace                  | 162 ms                                                          | 175 ms: 1.08x slower                                                        |
| tomli_loads               | 1.35 sec                                                        | 1.46 sec: 1.08x slower                                                      |
| docutils                  | 1.63 sec                                                        | 1.75 sec: 1.08x slower                                                      |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.61 sec: 1.09x slower                                                      |
| mypy2                     | 418 ms                                                          | 454 ms: 1.09x slower                                                        |
| crypto_pyaes              | 45.5 ms                                                         | 49.5 ms: 1.09x slower                                                       |
| async_tree_none_tg        | 202 ms                                                          | 220 ms: 1.09x slower                                                        |
| sqlglot_normalize         | 173 ms                                                          | 189 ms: 1.09x slower                                                        |
| async_generators          | 223 ms                                                          | 245 ms: 1.10x slower                                                        |
| unpickle_list             | 2.62 us                                                         | 2.88 us: 1.10x slower                                                       |
| sqlglot_transpile         | 955 us                                                          | 1.05 ms: 1.10x slower                                                       |
| coverage                  | 42.1 ms                                                         | 46.4 ms: 1.10x slower                                                       |
| sqlglot_parse             | 748 us                                                          | 829 us: 1.11x slower                                                        |
| sympy_sum                 | 84.4 ms                                                         | 93.8 ms: 1.11x slower                                                       |
| mako                      | 6.36 ms                                                         | 7.07 ms: 1.11x slower                                                       |
| pprint_safe_repr          | 474 ms                                                          | 532 ms: 1.12x slower                                                        |
| sqlglot_optimize          | 32.7 ms                                                         | 36.8 ms: 1.13x slower                                                       |
| fannkuch                  | 243 ms                                                          | 274 ms: 1.13x slower                                                        |
| sympy_integrate           | 12.2 ms                                                         | 13.8 ms: 1.13x slower                                                       |
| pprint_pformat            | 966 ms                                                          | 1.09 sec: 1.13x slower                                                      |
| sympy_expand              | 271 ms                                                          | 307 ms: 1.13x slower                                                        |
| genshi_xml                | 31.6 ms                                                         | 35.8 ms: 1.13x slower                                                       |
| thrift                    | 8.11 ms                                                         | 9.24 ms: 1.14x slower                                                       |
| sympy_str                 | 159 ms                                                          | 182 ms: 1.14x slower                                                        |
| float                     | 49.7 ms                                                         | 57.0 ms: 1.15x slower                                                       |
| chaos                     | 38.4 ms                                                         | 44.2 ms: 1.15x slower                                                       |
| generators                | 19.6 ms                                                         | 22.6 ms: 1.16x slower                                                       |
| genshi_text               | 14.4 ms                                                         | 16.7 ms: 1.16x slower                                                       |
| dulwich_log               | 38.0 ms                                                         | 44.3 ms: 1.17x slower                                                       |
| scimark_fft               | 171 ms                                                          | 199 ms: 1.17x slower                                                        |
| nbody                     | 67.6 ms                                                         | 79.3 ms: 1.17x slower                                                       |
| scimark_sor               | 75.3 ms                                                         | 89.4 ms: 1.19x slower                                                       |
| mdp                       | 1.31 sec                                                        | 1.56 sec: 1.19x slower                                                      |
| pyflate                   | 279 ms                                                          | 332 ms: 1.19x slower                                                        |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 3.08 ms: 1.23x slower                                                       |
| go                        | 82.1 ms                                                         | 101 ms: 1.23x slower                                                        |
| spectral_norm             | 63.7 ms                                                         | 79.0 ms: 1.24x slower                                                       |
| scimark_monte_carlo       | 39.1 ms                                                         | 49.0 ms: 1.25x slower                                                       |
| nqueens                   | 56.7 ms                                                         | 71.2 ms: 1.26x slower                                                       |
| unpickle_pure_python      | 122 us                                                          | 155 us: 1.27x slower                                                        |
| deltablue                 | 1.88 ms                                                         | 2.44 ms: 1.29x slower                                                       |
| regex_compile             | 78.0 ms                                                         | 103 ms: 1.32x slower                                                        |
| comprehensions            | 10.4 us                                                         | 13.9 us: 1.33x slower                                                       |
| scimark_lu                | 56.6 ms                                                         | 78.6 ms: 1.39x slower                                                       |
| hexiom                    | 3.72 ms                                                         | 5.19 ms: 1.39x slower                                                       |
| Geometric mean            | (ref)                                                           | 1.08x slower                                                                |

Benchmark hidden because not significant (10): pylint, regex_v8, pycparser, python_startup_no_site, pathlib, async_tree_cpu_io_mixed_tg, gc_traversal, async_tree_cpu_io_mixed, async_tree_io, asyncio_tcp
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: unknown