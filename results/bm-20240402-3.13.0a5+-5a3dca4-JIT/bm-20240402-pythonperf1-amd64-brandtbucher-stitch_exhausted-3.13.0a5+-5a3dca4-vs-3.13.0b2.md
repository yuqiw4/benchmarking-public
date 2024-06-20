# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-amd64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.03x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 222 ms: 1.08x slower                                                          |
| chameleon      | 4.80 ms                                                         | 4.75 ms: 1.01x faster                                                         |
| docutils       | 1.63 sec                                                        | 1.73 sec: 1.06x slower                                                        |
| html5lib       | 35.0 ms                                                         | 36.8 ms: 1.05x slower                                                         |
| tornado_http   | 81.8 ms                                                         | 85.2 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                           | 1.04x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|---------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed   | 389 ms                                                          | 379 ms: 1.03x faster                                                          |
| async_tree_io_tg          | 605 ms                                                          | 615 ms: 1.02x slower                                                          |
| async_tree_memoization    | 264 ms                                                          | 273 ms: 1.03x slower                                                          |
| async_tree_memoization_tg | 258 ms                                                          | 270 ms: 1.04x slower                                                          |
| Geometric mean            | (ref)                                                           | 1.01x slower                                                                  |

Benchmark hidden because not significant (4): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 57.4 ms: 1.18x faster                                                         |
| float          | 49.7 ms                                                         | 46.6 ms: 1.07x faster                                                         |
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                          |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                          | 116 ms: 1.02x faster                                                          |
| regex_effbot   | 1.58 ms                                                         | 1.56 ms: 1.01x faster                                                         |
| regex_compile  | 78.0 ms                                                         | 87.5 ms: 1.12x slower                                                         |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                  |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.21 sec: 1.12x faster                                                        |
| json_loads           | 14.2 us                                                         | 13.7 us: 1.04x faster                                                         |
| json_dumps           | 5.61 ms                                                         | 5.51 ms: 1.02x faster                                                         |
| unpickle             | 8.40 us                                                         | 8.48 us: 1.01x slower                                                         |
| xml_etree_parse      | 90.9 ms                                                         | 92.1 ms: 1.01x slower                                                         |
| pickle_pure_python   | 175 us                                                          | 178 us: 1.02x slower                                                          |
| xml_etree_process    | 36.4 ms                                                         | 37.1 ms: 1.02x slower                                                         |
| xml_etree_iterparse  | 62.3 ms                                                         | 64.1 ms: 1.03x slower                                                         |
| xml_etree_generate   | 53.2 ms                                                         | 55.0 ms: 1.03x slower                                                         |
| pickle_dict          | 18.1 us                                                         | 18.8 us: 1.04x slower                                                         |
| pickle               | 7.11 us                                                         | 7.40 us: 1.04x slower                                                         |
| unpickle_pure_python | 122 us                                                          | 131 us: 1.08x slower                                                          |
| unpickle_list        | 2.62 us                                                         | 2.84 us: 1.09x slower                                                         |
| pickle_list          | 2.90 us                                                         | 3.17 us: 1.09x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.02x slower                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 21.9 ms: 1.08x slower                                                         |
| python_startup_no_site | 16.2 ms                                                         | 19.6 ms: 1.21x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.14x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 5.71 ms: 1.11x faster                                                         |
| genshi_text     | 14.4 ms                                                         | 15.6 ms: 1.09x slower                                                         |
| genshi_xml      | 31.6 ms                                                         | 34.6 ms: 1.10x slower                                                         |
| django_template | 21.7 ms                                                         | 24.3 ms: 1.12x slower                                                         |
| Geometric mean  | (ref)                                                           | 1.05x slower                                                                  |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|---------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 73.0 us: 1.38x faster                                                         |
| spectral_norm             | 63.7 ms                                                         | 51.2 ms: 1.24x faster                                                         |
| nbody                     | 67.6 ms                                                         | 57.4 ms: 1.18x faster                                                         |
| tomli_loads               | 1.35 sec                                                        | 1.21 sec: 1.12x faster                                                        |
| mako                      | 6.36 ms                                                         | 5.71 ms: 1.11x faster                                                         |
| json                      | 3.19 ms                                                         | 2.87 ms: 1.11x faster                                                         |
| pycparser                 | 754 ms                                                          | 684 ms: 1.10x faster                                                          |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.30 ms: 1.09x faster                                                         |
| float                     | 49.7 ms                                                         | 46.6 ms: 1.07x faster                                                         |
| fannkuch                  | 243 ms                                                          | 232 ms: 1.05x faster                                                          |
| create_gc_cycles          | 888 us                                                          | 856 us: 1.04x faster                                                          |
| json_loads                | 14.2 us                                                         | 13.7 us: 1.04x faster                                                         |
| deepcopy_memo             | 22.1 us                                                         | 21.5 us: 1.03x faster                                                         |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 379 ms: 1.03x faster                                                          |
| regex_dna                 | 119 ms                                                          | 116 ms: 1.02x faster                                                          |
| pidigits                  | 150 ms                                                          | 147 ms: 1.02x faster                                                          |
| json_dumps                | 5.61 ms                                                         | 5.51 ms: 1.02x faster                                                         |
| scimark_fft               | 171 ms                                                          | 168 ms: 1.02x faster                                                          |
| pprint_safe_repr          | 474 ms                                                          | 465 ms: 1.02x faster                                                          |
| sqlite_synth              | 1.60 us                                                         | 1.57 us: 1.02x faster                                                         |
| regex_effbot              | 1.58 ms                                                         | 1.56 ms: 1.01x faster                                                         |
| gc_traversal              | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                         |
| crypto_pyaes              | 45.5 ms                                                         | 45.0 ms: 1.01x faster                                                         |
| chameleon                 | 4.80 ms                                                         | 4.75 ms: 1.01x faster                                                         |
| pprint_pformat            | 966 ms                                                          | 961 ms: 1.01x faster                                                          |
| unpickle                  | 8.40 us                                                         | 8.48 us: 1.01x slower                                                         |
| telco                     | 4.67 ms                                                         | 4.72 ms: 1.01x slower                                                         |
| xml_etree_parse           | 90.9 ms                                                         | 92.1 ms: 1.01x slower                                                         |
| async_tree_io_tg          | 605 ms                                                          | 615 ms: 1.02x slower                                                          |
| pyflate                   | 279 ms                                                          | 283 ms: 1.02x slower                                                          |
| aiohttp                   | 889 us                                                          | 903 us: 1.02x slower                                                          |
| pickle_pure_python        | 175 us                                                          | 178 us: 1.02x slower                                                          |
| xml_etree_process         | 36.4 ms                                                         | 37.1 ms: 1.02x slower                                                         |
| logging_format            | 6.22 us                                                         | 6.36 us: 1.02x slower                                                         |
| logging_simple            | 5.78 us                                                         | 5.92 us: 1.02x slower                                                         |
| pathlib                   | 75.9 ms                                                         | 77.8 ms: 1.03x slower                                                         |
| deepcopy                  | 220 us                                                          | 225 us: 1.03x slower                                                          |
| xml_etree_iterparse       | 62.3 ms                                                         | 64.1 ms: 1.03x slower                                                         |
| chaos                     | 38.4 ms                                                         | 39.5 ms: 1.03x slower                                                         |
| async_tree_memoization    | 264 ms                                                          | 273 ms: 1.03x slower                                                          |
| xml_etree_generate        | 53.2 ms                                                         | 55.0 ms: 1.03x slower                                                         |
| pickle_dict               | 18.1 us                                                         | 18.8 us: 1.04x slower                                                         |
| coroutines                | 12.8 ms                                                         | 13.2 ms: 1.04x slower                                                         |
| richards_super            | 30.2 ms                                                         | 31.3 ms: 1.04x slower                                                         |
| logging_silent            | 52.9 ns                                                         | 55.0 ns: 1.04x slower                                                         |
| pickle                    | 7.11 us                                                         | 7.40 us: 1.04x slower                                                         |
| tornado_http              | 81.8 ms                                                         | 85.2 ms: 1.04x slower                                                         |
| sqlglot_parse             | 748 us                                                          | 780 us: 1.04x slower                                                          |
| generators                | 19.6 ms                                                         | 20.4 ms: 1.04x slower                                                         |
| async_tree_memoization_tg | 258 ms                                                          | 270 ms: 1.04x slower                                                          |
| bench_mp_pool             | 64.8 ms                                                         | 67.8 ms: 1.05x slower                                                         |
| scimark_monte_carlo       | 39.1 ms                                                         | 41.1 ms: 1.05x slower                                                         |
| html5lib                  | 35.0 ms                                                         | 36.8 ms: 1.05x slower                                                         |
| sqlglot_transpile         | 955 us                                                          | 1.01 ms: 1.06x slower                                                         |
| richards                  | 26.7 ms                                                         | 28.2 ms: 1.06x slower                                                         |
| scimark_sor               | 75.3 ms                                                         | 80.0 ms: 1.06x slower                                                         |
| docutils                  | 1.63 sec                                                        | 1.73 sec: 1.06x slower                                                        |
| comprehensions            | 10.4 us                                                         | 11.1 us: 1.06x slower                                                         |
| sympy_sum                 | 84.4 ms                                                         | 90.1 ms: 1.07x slower                                                         |
| dulwich_log               | 38.0 ms                                                         | 40.9 ms: 1.07x slower                                                         |
| meteor_contest            | 69.9 ms                                                         | 75.1 ms: 1.07x slower                                                         |
| 2to3                      | 207 ms                                                          | 222 ms: 1.08x slower                                                          |
| unpickle_pure_python      | 122 us                                                          | 131 us: 1.08x slower                                                          |
| python_startup            | 20.3 ms                                                         | 21.9 ms: 1.08x slower                                                         |
| sympy_str                 | 159 ms                                                          | 172 ms: 1.08x slower                                                          |
| sqlglot_normalize         | 173 ms                                                          | 187 ms: 1.08x slower                                                          |
| async_generators          | 223 ms                                                          | 242 ms: 1.08x slower                                                          |
| bench_thread_pool         | 768 us                                                          | 833 us: 1.09x slower                                                          |
| unpickle_list             | 2.62 us                                                         | 2.84 us: 1.09x slower                                                         |
| genshi_text               | 14.4 ms                                                         | 15.6 ms: 1.09x slower                                                         |
| pickle_list               | 2.90 us                                                         | 3.17 us: 1.09x slower                                                         |
| sympy_expand              | 271 ms                                                          | 296 ms: 1.09x slower                                                          |
| deltablue                 | 1.88 ms                                                         | 2.06 ms: 1.10x slower                                                         |
| sqlglot_optimize          | 32.7 ms                                                         | 35.9 ms: 1.10x slower                                                         |
| genshi_xml                | 31.6 ms                                                         | 34.6 ms: 1.10x slower                                                         |
| coverage                  | 42.1 ms                                                         | 46.3 ms: 1.10x slower                                                         |
| nqueens                   | 56.7 ms                                                         | 62.5 ms: 1.10x slower                                                         |
| sympy_integrate           | 12.2 ms                                                         | 13.6 ms: 1.11x slower                                                         |
| django_template           | 21.7 ms                                                         | 24.3 ms: 1.12x slower                                                         |
| regex_compile             | 78.0 ms                                                         | 87.5 ms: 1.12x slower                                                         |
| mypy2                     | 418 ms                                                          | 471 ms: 1.13x slower                                                          |
| mdp                       | 1.31 sec                                                        | 1.49 sec: 1.14x slower                                                        |
| thrift                    | 8.11 ms                                                         | 9.22 ms: 1.14x slower                                                         |
| raytrace                  | 162 ms                                                          | 185 ms: 1.14x slower                                                          |
| go                        | 82.1 ms                                                         | 97.7 ms: 1.19x slower                                                         |
| python_startup_no_site    | 16.2 ms                                                         | 19.6 ms: 1.21x slower                                                         |
| scimark_lu                | 56.6 ms                                                         | 73.2 ms: 1.29x slower                                                         |
| hexiom                    | 3.72 ms                                                         | 4.92 ms: 1.32x slower                                                         |
| Geometric mean            | (ref)                                                           | 1.03x slower                                                                  |

Benchmark hidden because not significant (9): asyncio_tcp_ssl, regex_v8, async_tree_io, pylint, deepcopy_reduce, async_tree_cpu_io_mixed_tg, asyncio_tcp, async_tree_none, async_tree_none_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: unknown