# Results vs. 3.13.0b2

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.11x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 226 ms: 1.09x slower                                                        |
| chameleon      | 4.80 ms                                                         | 5.06 ms: 1.05x slower                                                       |
| docutils       | 1.63 sec                                                        | 1.76 sec: 1.08x slower                                                      |
| html5lib       | 35.0 ms                                                         | 37.9 ms: 1.08x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 86.2 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                           | 1.07x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg          | 605 ms                                                          | 622 ms: 1.03x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 277 ms: 1.05x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 272 ms: 1.05x slower                                                        |
| async_tree_none           | 218 ms                                                          | 230 ms: 1.06x slower                                                        |
| async_tree_none_tg        | 202 ms                                                          | 221 ms: 1.09x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 148 ms: 1.01x faster                                                        |
| float          | 49.7 ms                                                         | 60.0 ms: 1.21x slower                                                       |
| nbody          | 67.6 ms                                                         | 83.2 ms: 1.23x slower                                                       |
| Geometric mean | (ref)                                                           | 1.14x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                          | 121 ms: 1.02x slower                                                        |
| regex_compile  | 78.0 ms                                                         | 107 ms: 1.38x slower                                                        |
| Geometric mean | (ref)                                                           | 1.08x slower                                                                |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| unpickle             | 8.40 us                                                         | 8.54 us: 1.02x slower                                                       |
| json_dumps           | 5.61 ms                                                         | 5.77 ms: 1.03x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 19.0 us: 1.04x slower                                                       |
| pickle_pure_python   | 175 us                                                          | 184 us: 1.05x slower                                                        |
| pickle               | 7.11 us                                                         | 7.50 us: 1.05x slower                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 56.6 ms: 1.06x slower                                                       |
| xml_etree_process    | 36.4 ms                                                         | 39.1 ms: 1.07x slower                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 67.8 ms: 1.09x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.88 us: 1.10x slower                                                       |
| tomli_loads          | 1.35 sec                                                        | 1.52 sec: 1.13x slower                                                      |
| unpickle_pure_python | 122 us                                                          | 169 us: 1.39x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.07x slower                                                                |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 20.1 ms: 1.01x faster                                                       |
| python_startup_no_site | 16.2 ms                                                         | 18.1 ms: 1.12x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.05x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 6.36 ms                                                         | 7.47 ms: 1.17x slower                                                       |
| genshi_xml     | 31.6 ms                                                         | 37.1 ms: 1.18x slower                                                       |
| genshi_text    | 14.4 ms                                                         | 17.0 ms: 1.18x slower                                                       |
| Geometric mean | (ref)                                                           | 1.18x slower                                                                |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 78.3 us: 1.29x faster                                                       |
| json                      | 3.19 ms                                                         | 2.88 ms: 1.10x faster                                                       |
| json_loads                | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| pidigits                  | 150 ms                                                          | 148 ms: 1.01x faster                                                        |
| python_startup            | 20.3 ms                                                         | 20.1 ms: 1.01x faster                                                       |
| gc_traversal              | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                       |
| sqlite_synth              | 1.60 us                                                         | 1.62 us: 1.01x slower                                                       |
| bench_mp_pool             | 64.8 ms                                                         | 65.7 ms: 1.01x slower                                                       |
| unpickle                  | 8.40 us                                                         | 8.54 us: 1.02x slower                                                       |
| regex_dna                 | 119 ms                                                          | 121 ms: 1.02x slower                                                        |
| coroutines                | 12.8 ms                                                         | 13.1 ms: 1.02x slower                                                       |
| async_tree_io_tg          | 605 ms                                                          | 622 ms: 1.03x slower                                                        |
| json_dumps                | 5.61 ms                                                         | 5.77 ms: 1.03x slower                                                       |
| pathlib                   | 75.9 ms                                                         | 78.0 ms: 1.03x slower                                                       |
| create_gc_cycles          | 888 us                                                          | 915 us: 1.03x slower                                                        |
| aiohttp                   | 889 us                                                          | 919 us: 1.03x slower                                                        |
| deepcopy_reduce           | 1.99 us                                                         | 2.08 us: 1.04x slower                                                       |
| pickle_dict               | 18.1 us                                                         | 19.0 us: 1.04x slower                                                       |
| pickle_pure_python        | 175 us                                                          | 184 us: 1.05x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 277 ms: 1.05x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 272 ms: 1.05x slower                                                        |
| chameleon                 | 4.80 ms                                                         | 5.06 ms: 1.05x slower                                                       |
| tornado_http              | 81.8 ms                                                         | 86.2 ms: 1.05x slower                                                       |
| pickle                    | 7.11 us                                                         | 7.50 us: 1.05x slower                                                       |
| async_tree_none           | 218 ms                                                          | 230 ms: 1.06x slower                                                        |
| telco                     | 4.67 ms                                                         | 4.96 ms: 1.06x slower                                                       |
| xml_etree_generate        | 53.2 ms                                                         | 56.6 ms: 1.06x slower                                                       |
| logging_silent            | 52.9 ns                                                         | 56.4 ns: 1.07x slower                                                       |
| deepcopy                  | 220 us                                                          | 235 us: 1.07x slower                                                        |
| xml_etree_process         | 36.4 ms                                                         | 39.1 ms: 1.07x slower                                                       |
| docutils                  | 1.63 sec                                                        | 1.76 sec: 1.08x slower                                                      |
| html5lib                  | 35.0 ms                                                         | 37.9 ms: 1.08x slower                                                       |
| richards                  | 26.7 ms                                                         | 29.0 ms: 1.09x slower                                                       |
| bench_thread_pool         | 768 us                                                          | 835 us: 1.09x slower                                                        |
| xml_etree_iterparse       | 62.3 ms                                                         | 67.8 ms: 1.09x slower                                                       |
| 2to3                      | 207 ms                                                          | 226 ms: 1.09x slower                                                        |
| raytrace                  | 162 ms                                                          | 177 ms: 1.09x slower                                                        |
| async_generators          | 223 ms                                                          | 244 ms: 1.09x slower                                                        |
| coverage                  | 42.1 ms                                                         | 46.0 ms: 1.09x slower                                                       |
| async_tree_none_tg        | 202 ms                                                          | 221 ms: 1.09x slower                                                        |
| richards_super            | 30.2 ms                                                         | 33.0 ms: 1.09x slower                                                       |
| unpickle_list             | 2.62 us                                                         | 2.88 us: 1.10x slower                                                       |
| meteor_contest            | 69.9 ms                                                         | 77.1 ms: 1.10x slower                                                       |
| sqlglot_transpile         | 955 us                                                          | 1.05 ms: 1.10x slower                                                       |
| logging_format            | 6.22 us                                                         | 6.87 us: 1.10x slower                                                       |
| mypy2                     | 418 ms                                                          | 462 ms: 1.11x slower                                                        |
| logging_simple            | 5.78 us                                                         | 6.42 us: 1.11x slower                                                       |
| mdp                       | 1.31 sec                                                        | 1.47 sec: 1.12x slower                                                      |
| python_startup_no_site    | 16.2 ms                                                         | 18.1 ms: 1.12x slower                                                       |
| sqlglot_parse             | 748 us                                                          | 838 us: 1.12x slower                                                        |
| tomli_loads               | 1.35 sec                                                        | 1.52 sec: 1.13x slower                                                      |
| sympy_sum                 | 84.4 ms                                                         | 95.3 ms: 1.13x slower                                                       |
| sqlglot_normalize         | 173 ms                                                          | 196 ms: 1.13x slower                                                        |
| deepcopy_memo             | 22.1 us                                                         | 25.1 us: 1.14x slower                                                       |
| crypto_pyaes              | 45.5 ms                                                         | 52.1 ms: 1.15x slower                                                       |
| sympy_expand              | 271 ms                                                          | 312 ms: 1.15x slower                                                        |
| sympy_integrate           | 12.2 ms                                                         | 14.1 ms: 1.15x slower                                                       |
| sqlglot_optimize          | 32.7 ms                                                         | 37.9 ms: 1.16x slower                                                       |
| generators                | 19.6 ms                                                         | 22.8 ms: 1.16x slower                                                       |
| pprint_pformat            | 966 ms                                                          | 1.13 sec: 1.17x slower                                                      |
| pprint_safe_repr          | 474 ms                                                          | 553 ms: 1.17x slower                                                        |
| thrift                    | 8.11 ms                                                         | 9.47 ms: 1.17x slower                                                       |
| sympy_str                 | 159 ms                                                          | 186 ms: 1.17x slower                                                        |
| mako                      | 6.36 ms                                                         | 7.47 ms: 1.17x slower                                                       |
| genshi_xml                | 31.6 ms                                                         | 37.1 ms: 1.18x slower                                                       |
| dulwich_log               | 38.0 ms                                                         | 45.0 ms: 1.18x slower                                                       |
| genshi_text               | 14.4 ms                                                         | 17.0 ms: 1.18x slower                                                       |
| chaos                     | 38.4 ms                                                         | 45.9 ms: 1.20x slower                                                       |
| float                     | 49.7 ms                                                         | 60.0 ms: 1.21x slower                                                       |
| fannkuch                  | 243 ms                                                          | 296 ms: 1.22x slower                                                        |
| pyflate                   | 279 ms                                                          | 341 ms: 1.22x slower                                                        |
| scimark_sor               | 75.3 ms                                                         | 92.4 ms: 1.23x slower                                                       |
| nbody                     | 67.6 ms                                                         | 83.2 ms: 1.23x slower                                                       |
| scimark_fft               | 171 ms                                                          | 212 ms: 1.24x slower                                                        |
| go                        | 82.1 ms                                                         | 104 ms: 1.27x slower                                                        |
| nqueens                   | 56.7 ms                                                         | 72.0 ms: 1.27x slower                                                       |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 3.28 ms: 1.31x slower                                                       |
| scimark_monte_carlo       | 39.1 ms                                                         | 52.2 ms: 1.33x slower                                                       |
| deltablue                 | 1.88 ms                                                         | 2.54 ms: 1.35x slower                                                       |
| spectral_norm             | 63.7 ms                                                         | 86.6 ms: 1.36x slower                                                       |
| regex_compile             | 78.0 ms                                                         | 107 ms: 1.38x slower                                                        |
| unpickle_pure_python      | 122 us                                                          | 169 us: 1.39x slower                                                        |
| comprehensions            | 10.4 us                                                         | 14.6 us: 1.40x slower                                                       |
| scimark_lu                | 56.6 ms                                                         | 81.2 ms: 1.43x slower                                                       |
| hexiom                    | 3.72 ms                                                         | 5.54 ms: 1.49x slower                                                       |
| Geometric mean            | (ref)                                                           | 1.11x slower                                                                |

Benchmark hidden because not significant (11): regex_v8, pycparser, pylint, regex_effbot, async_tree_cpu_io_mixed_tg, xml_etree_parse, async_tree_io, pickle_list, async_tree_cpu_io_mixed, asyncio_tcp, asyncio_tcp_ssl
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: unknown