# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_binary_op
- machine: windows-amd64
- commit hash: 8183250
- commit date: 2024-03-27
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-pythonperf1-amd64-faster%2dcpython-specialize_binary_op-3.13.0a5+-8183250 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 213 ms: 1.03x slower                                                                  |
| chameleon      | 4.80 ms                                                         | 4.76 ms: 1.01x faster                                                                 |
| html5lib       | 35.0 ms                                                         | 36.5 ms: 1.04x slower                                                                 |
| tornado_http   | 81.8 ms                                                         | 84.0 ms: 1.03x slower                                                                 |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-pythonperf1-amd64-faster%2dcpython-specialize_binary_op-3.13.0a5+-8183250 |
|---------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| async_tree_io_tg          | 605 ms                                                          | 562 ms: 1.08x faster                                                                  |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 382 ms: 1.02x faster                                                                  |
| async_tree_none           | 218 ms                                                          | 223 ms: 1.02x slower                                                                  |
| async_tree_none_tg        | 202 ms                                                          | 210 ms: 1.04x slower                                                                  |
| async_tree_memoization_tg | 258 ms                                                          | 269 ms: 1.04x slower                                                                  |
| async_tree_memoization    | 264 ms                                                          | 276 ms: 1.05x slower                                                                  |
| Geometric mean            | (ref)                                                           | 1.01x slower                                                                          |

Benchmark hidden because not significant (2): async_tree_io, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-pythonperf1-amd64-faster%2dcpython-specialize_binary_op-3.13.0a5+-8183250 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                                  |
| float          | 49.7 ms                                                         | 51.8 ms: 1.04x slower                                                                 |
| nbody          | 67.6 ms                                                         | 77.5 ms: 1.15x slower                                                                 |
| Geometric mean | (ref)                                                           | 1.05x slower                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-pythonperf1-amd64-faster%2dcpython-specialize_binary_op-3.13.0a5+-8183250 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                          | 115 ms: 1.03x faster                                                                  |
| regex_effbot   | 1.58 ms                                                         | 1.55 ms: 1.02x faster                                                                 |
| regex_compile  | 78.0 ms                                                         | 81.3 ms: 1.04x slower                                                                 |
| Geometric mean | (ref)                                                           | 1.00x slower                                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-pythonperf1-amd64-faster%2dcpython-specialize_binary_op-3.13.0a5+-8183250 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| json_dumps           | 5.61 ms                                                         | 5.55 ms: 1.01x faster                                                                 |
| json_loads           | 14.2 us                                                         | 14.1 us: 1.01x faster                                                                 |
| unpickle             | 8.40 us                                                         | 8.47 us: 1.01x slower                                                                 |
| pickle_pure_python   | 175 us                                                          | 179 us: 1.02x slower                                                                  |
| xml_etree_generate   | 53.2 ms                                                         | 54.3 ms: 1.02x slower                                                                 |
| pickle               | 7.11 us                                                         | 7.26 us: 1.02x slower                                                                 |
| xml_etree_iterparse  | 62.3 ms                                                         | 63.7 ms: 1.02x slower                                                                 |
| xml_etree_process    | 36.4 ms                                                         | 37.3 ms: 1.02x slower                                                                 |
| xml_etree_parse      | 90.9 ms                                                         | 93.8 ms: 1.03x slower                                                                 |
| unpickle_pure_python | 122 us                                                          | 127 us: 1.04x slower                                                                  |
| unpickle_list        | 2.62 us                                                         | 2.82 us: 1.08x slower                                                                 |
| tomli_loads          | 1.35 sec                                                        | 1.47 sec: 1.09x slower                                                                |
| Geometric mean       | (ref)                                                           | 1.02x slower                                                                          |

Benchmark hidden because not significant (2): pickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-pythonperf1-amd64-faster%2dcpython-specialize_binary_op-3.13.0a5+-8183250 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                         | 17.9 ms: 1.11x slower                                                                 |
| Geometric mean         | (ref)                                                           | 1.05x slower                                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-pythonperf1-amd64-faster%2dcpython-specialize_binary_op-3.13.0a5+-8183250 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| django_template | 21.7 ms                                                         | 22.6 ms: 1.04x slower                                                                 |
| genshi_text     | 14.4 ms                                                         | 15.8 ms: 1.10x slower                                                                 |
| genshi_xml      | 31.6 ms                                                         | 35.0 ms: 1.11x slower                                                                 |
| Geometric mean  | (ref)                                                           | 1.06x slower                                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-pythonperf1-amd64-faster%2dcpython-specialize_binary_op-3.13.0a5+-8183250 |
|---------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 71.6 us: 1.41x faster                                                                 |
| create_gc_cycles          | 888 us                                                          | 729 us: 1.22x faster                                                                  |
| pycparser                 | 754 ms                                                          | 684 ms: 1.10x faster                                                                  |
| json                      | 3.19 ms                                                         | 2.92 ms: 1.09x faster                                                                 |
| async_tree_io_tg          | 605 ms                                                          | 562 ms: 1.08x faster                                                                  |
| gc_traversal              | 1.55 ms                                                         | 1.48 ms: 1.05x faster                                                                 |
| regex_dna                 | 119 ms                                                          | 115 ms: 1.03x faster                                                                  |
| deepcopy_reduce           | 1.99 us                                                         | 1.94 us: 1.03x faster                                                                 |
| regex_effbot              | 1.58 ms                                                         | 1.55 ms: 1.02x faster                                                                 |
| pidigits                  | 150 ms                                                          | 147 ms: 1.02x faster                                                                  |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 382 ms: 1.02x faster                                                                  |
| deepcopy_memo             | 22.1 us                                                         | 21.7 us: 1.02x faster                                                                 |
| bench_mp_pool             | 64.8 ms                                                         | 63.9 ms: 1.01x faster                                                                 |
| json_dumps                | 5.61 ms                                                         | 5.55 ms: 1.01x faster                                                                 |
| deepcopy                  | 220 us                                                          | 217 us: 1.01x faster                                                                  |
| sympy_sum                 | 84.4 ms                                                         | 83.5 ms: 1.01x faster                                                                 |
| json_loads                | 14.2 us                                                         | 14.1 us: 1.01x faster                                                                 |
| chameleon                 | 4.80 ms                                                         | 4.76 ms: 1.01x faster                                                                 |
| sympy_integrate           | 12.2 ms                                                         | 12.3 ms: 1.01x slower                                                                 |
| unpickle                  | 8.40 us                                                         | 8.47 us: 1.01x slower                                                                 |
| scimark_lu                | 56.6 ms                                                         | 57.1 ms: 1.01x slower                                                                 |
| thrift                    | 8.11 ms                                                         | 8.20 ms: 1.01x slower                                                                 |
| hexiom                    | 3.72 ms                                                         | 3.78 ms: 1.01x slower                                                                 |
| aiohttp                   | 889 us                                                          | 901 us: 1.01x slower                                                                  |
| sqlite_synth              | 1.60 us                                                         | 1.62 us: 1.01x slower                                                                 |
| pickle_pure_python        | 175 us                                                          | 179 us: 1.02x slower                                                                  |
| pprint_pformat            | 966 ms                                                          | 985 ms: 1.02x slower                                                                  |
| xml_etree_generate        | 53.2 ms                                                         | 54.3 ms: 1.02x slower                                                                 |
| pickle                    | 7.11 us                                                         | 7.26 us: 1.02x slower                                                                 |
| pathlib                   | 75.9 ms                                                         | 77.5 ms: 1.02x slower                                                                 |
| xml_etree_iterparse       | 62.3 ms                                                         | 63.7 ms: 1.02x slower                                                                 |
| pprint_safe_repr          | 474 ms                                                          | 485 ms: 1.02x slower                                                                  |
| async_tree_none           | 218 ms                                                          | 223 ms: 1.02x slower                                                                  |
| meteor_contest            | 69.9 ms                                                         | 71.5 ms: 1.02x slower                                                                 |
| xml_etree_process         | 36.4 ms                                                         | 37.3 ms: 1.02x slower                                                                 |
| crypto_pyaes              | 45.5 ms                                                         | 46.7 ms: 1.03x slower                                                                 |
| tornado_http              | 81.8 ms                                                         | 84.0 ms: 1.03x slower                                                                 |
| sqlglot_normalize         | 173 ms                                                          | 178 ms: 1.03x slower                                                                  |
| 2to3                      | 207 ms                                                          | 213 ms: 1.03x slower                                                                  |
| xml_etree_parse           | 90.9 ms                                                         | 93.8 ms: 1.03x slower                                                                 |
| sqlglot_optimize          | 32.7 ms                                                         | 33.8 ms: 1.03x slower                                                                 |
| comprehensions            | 10.4 us                                                         | 10.7 us: 1.03x slower                                                                 |
| sqlglot_transpile         | 955 us                                                          | 990 us: 1.04x slower                                                                  |
| async_tree_none_tg        | 202 ms                                                          | 210 ms: 1.04x slower                                                                  |
| raytrace                  | 162 ms                                                          | 169 ms: 1.04x slower                                                                  |
| unpickle_pure_python      | 122 us                                                          | 127 us: 1.04x slower                                                                  |
| float                     | 49.7 ms                                                         | 51.8 ms: 1.04x slower                                                                 |
| django_template           | 21.7 ms                                                         | 22.6 ms: 1.04x slower                                                                 |
| regex_compile             | 78.0 ms                                                         | 81.3 ms: 1.04x slower                                                                 |
| bench_thread_pool         | 768 us                                                          | 801 us: 1.04x slower                                                                  |
| async_tree_memoization_tg | 258 ms                                                          | 269 ms: 1.04x slower                                                                  |
| html5lib                  | 35.0 ms                                                         | 36.5 ms: 1.04x slower                                                                 |
| async_generators          | 223 ms                                                          | 233 ms: 1.04x slower                                                                  |
| telco                     | 4.67 ms                                                         | 4.88 ms: 1.04x slower                                                                 |
| async_tree_memoization    | 264 ms                                                          | 276 ms: 1.05x slower                                                                  |
| sqlglot_parse             | 748 us                                                          | 784 us: 1.05x slower                                                                  |
| mypy2                     | 418 ms                                                          | 438 ms: 1.05x slower                                                                  |
| richards_super            | 30.2 ms                                                         | 32.0 ms: 1.06x slower                                                                 |
| logging_format            | 6.22 us                                                         | 6.65 us: 1.07x slower                                                                 |
| logging_simple            | 5.78 us                                                         | 6.18 us: 1.07x slower                                                                 |
| logging_silent            | 52.9 ns                                                         | 56.6 ns: 1.07x slower                                                                 |
| richards                  | 26.7 ms                                                         | 28.6 ms: 1.07x slower                                                                 |
| dulwich_log               | 38.0 ms                                                         | 40.9 ms: 1.07x slower                                                                 |
| unpickle_list             | 2.62 us                                                         | 2.82 us: 1.08x slower                                                                 |
| go                        | 82.1 ms                                                         | 88.4 ms: 1.08x slower                                                                 |
| deltablue                 | 1.88 ms                                                         | 2.04 ms: 1.08x slower                                                                 |
| pyflate                   | 279 ms                                                          | 302 ms: 1.08x slower                                                                  |
| scimark_monte_carlo       | 39.1 ms                                                         | 42.6 ms: 1.09x slower                                                                 |
| tomli_loads               | 1.35 sec                                                        | 1.47 sec: 1.09x slower                                                                |
| nqueens                   | 56.7 ms                                                         | 62.0 ms: 1.09x slower                                                                 |
| chaos                     | 38.4 ms                                                         | 42.0 ms: 1.10x slower                                                                 |
| genshi_text               | 14.4 ms                                                         | 15.8 ms: 1.10x slower                                                                 |
| python_startup_no_site    | 16.2 ms                                                         | 17.9 ms: 1.11x slower                                                                 |
| genshi_xml                | 31.6 ms                                                         | 35.0 ms: 1.11x slower                                                                 |
| generators                | 19.6 ms                                                         | 21.7 ms: 1.11x slower                                                                 |
| coverage                  | 42.1 ms                                                         | 46.8 ms: 1.11x slower                                                                 |
| mdp                       | 1.31 sec                                                        | 1.46 sec: 1.11x slower                                                                |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.81 ms: 1.12x slower                                                                 |
| fannkuch                  | 243 ms                                                          | 274 ms: 1.12x slower                                                                  |
| coroutines                | 12.8 ms                                                         | 14.4 ms: 1.13x slower                                                                 |
| scimark_sor               | 75.3 ms                                                         | 85.2 ms: 1.13x slower                                                                 |
| nbody                     | 67.6 ms                                                         | 77.5 ms: 1.15x slower                                                                 |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.74 sec: 1.18x slower                                                                |
| spectral_norm             | 63.7 ms                                                         | 75.0 ms: 1.18x slower                                                                 |
| scimark_fft               | 171 ms                                                          | 209 ms: 1.22x slower                                                                  |
| Geometric mean            | (ref)                                                           | 1.03x slower                                                                          |

Benchmark hidden because not significant (12): pickle_list, async_tree_io, sympy_expand, sympy_str, mako, pickle_dict, docutils, async_tree_cpu_io_mixed_tg, python_startup, asyncio_tcp, pylint, regex_v8
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240327-3.13.0a5+-8183250/bm-20240327-pythonperf1-amd64-faster%2dcpython-specialize_binary_op-3.13.0a5+-8183250.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: unknown