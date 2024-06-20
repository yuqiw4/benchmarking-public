# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 306 ms: 1.05x slower                                                           |
| chameleon      | 7.40 ms                                                          | 7.57 ms: 1.02x slower                                                          |
| docutils       | 2.98 sec                                                         | 3.13 sec: 1.05x slower                                                         |
| tornado_http   | 119 ms                                                           | 124 ms: 1.04x slower                                                           |
| Geometric mean | (ref)                                                            | 1.03x slower                                                                   |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|---------------------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_io_tg          | 900 ms                                                           | 910 ms: 1.01x slower                                                           |
| async_tree_memoization_tg | 421 ms                                                           | 437 ms: 1.04x slower                                                           |
| Geometric mean            | (ref)                                                            | 1.00x slower                                                                   |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 79.0 ms: 1.01x faster                                                          |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                           |
| nbody          | 87.8 ms                                                          | 96.8 ms: 1.10x slower                                                          |
| Geometric mean | (ref)                                                            | 1.04x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 240 ms: 1.04x faster                                                           |
| regex_v8       | 26.0 ms                                                          | 25.7 ms: 1.01x faster                                                          |
| regex_compile  | 144 ms                                                           | 146 ms: 1.01x slower                                                           |
| regex_effbot   | 3.40 ms                                                          | 3.60 ms: 1.06x slower                                                          |
| Geometric mean | (ref)                                                            | 1.00x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.16 sec: 1.11x faster                                                         |
| unpickle             | 15.7 us                                                          | 15.1 us: 1.04x faster                                                          |
| xml_etree_generate   | 85.7 ms                                                          | 82.7 ms: 1.04x faster                                                          |
| xml_etree_process    | 59.7 ms                                                          | 58.2 ms: 1.03x faster                                                          |
| unpickle_list        | 4.70 us                                                          | 4.61 us: 1.02x faster                                                          |
| xml_etree_parse      | 144 ms                                                           | 142 ms: 1.01x faster                                                           |
| xml_etree_iterparse  | 103 ms                                                           | 102 ms: 1.01x faster                                                           |
| pickle_dict          | 32.8 us                                                          | 33.0 us: 1.01x slower                                                          |
| pickle_list          | 4.44 us                                                          | 4.50 us: 1.01x slower                                                          |
| json_loads           | 25.0 us                                                          | 25.4 us: 1.02x slower                                                          |
| unpickle_pure_python | 224 us                                                           | 230 us: 1.03x slower                                                           |
| pickle               | 10.6 us                                                          | 11.0 us: 1.04x slower                                                          |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                                   |

Benchmark hidden because not significant (2): json_dumps, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                          |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                          |
| Geometric mean         | (ref)                                                            | 1.17x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 9.90 ms: 1.05x faster                                                          |
| genshi_xml      | 58.1 ms                                                          | 59.9 ms: 1.03x slower                                                          |
| django_template | 39.0 ms                                                          | 40.9 ms: 1.05x slower                                                          |
| genshi_text     | 25.9 ms                                                          | 28.0 ms: 1.08x slower                                                          |
| Geometric mean  | (ref)                                                            | 1.03x slower                                                                   |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|---------------------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols  | 171 us                                                           | 123 us: 1.39x faster                                                           |
| tomli_loads               | 2.40 sec                                                         | 2.16 sec: 1.11x faster                                                         |
| create_gc_cycles          | 2.00 ms                                                          | 1.81 ms: 1.11x faster                                                          |
| gc_traversal              | 4.69 ms                                                          | 4.35 ms: 1.08x faster                                                          |
| richards_super            | 61.2 ms                                                          | 57.6 ms: 1.06x faster                                                          |
| richards                  | 53.4 ms                                                          | 50.5 ms: 1.06x faster                                                          |
| mako                      | 10.4 ms                                                          | 9.90 ms: 1.05x faster                                                          |
| regex_dna                 | 249 ms                                                           | 240 ms: 1.04x faster                                                           |
| unpickle                  | 15.7 us                                                          | 15.1 us: 1.04x faster                                                          |
| sqlite_synth              | 2.80 us                                                          | 2.70 us: 1.04x faster                                                          |
| xml_etree_generate        | 85.7 ms                                                          | 82.7 ms: 1.04x faster                                                          |
| spectral_norm             | 97.3 ms                                                          | 94.0 ms: 1.04x faster                                                          |
| telco                     | 8.40 ms                                                          | 8.11 ms: 1.03x faster                                                          |
| scimark_sparse_mat_mult   | 4.28 ms                                                          | 4.14 ms: 1.03x faster                                                          |
| asyncio_websockets        | 395 ms                                                           | 384 ms: 1.03x faster                                                           |
| xml_etree_process         | 59.7 ms                                                          | 58.2 ms: 1.03x faster                                                          |
| unpickle_list             | 4.70 us                                                          | 4.61 us: 1.02x faster                                                          |
| float                     | 80.2 ms                                                          | 79.0 ms: 1.01x faster                                                          |
| regex_v8                  | 26.0 ms                                                          | 25.7 ms: 1.01x faster                                                          |
| xml_etree_parse           | 144 ms                                                           | 142 ms: 1.01x faster                                                           |
| asyncio_tcp               | 378 ms                                                           | 375 ms: 1.01x faster                                                           |
| xml_etree_iterparse       | 103 ms                                                           | 102 ms: 1.01x faster                                                           |
| pickle_dict               | 32.8 us                                                          | 33.0 us: 1.01x slower                                                          |
| coverage                  | 83.5 ms                                                          | 84.3 ms: 1.01x slower                                                          |
| coroutines                | 22.0 ms                                                          | 22.2 ms: 1.01x slower                                                          |
| regex_compile             | 144 ms                                                           | 146 ms: 1.01x slower                                                           |
| async_tree_io_tg          | 900 ms                                                           | 910 ms: 1.01x slower                                                           |
| pickle_list               | 4.44 us                                                          | 4.50 us: 1.01x slower                                                          |
| logging_silent            | 96.3 ns                                                          | 97.7 ns: 1.01x slower                                                          |
| json_loads                | 25.0 us                                                          | 25.4 us: 1.02x slower                                                          |
| pprint_safe_repr          | 818 ms                                                           | 836 ms: 1.02x slower                                                           |
| chameleon                 | 7.40 ms                                                          | 7.57 ms: 1.02x slower                                                          |
| python_startup            | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                          |
| dulwich_log               | 67.3 ms                                                          | 68.9 ms: 1.02x slower                                                          |
| unpickle_pure_python      | 224 us                                                           | 230 us: 1.03x slower                                                           |
| sqlglot_parse             | 1.39 ms                                                          | 1.43 ms: 1.03x slower                                                          |
| deepcopy_memo             | 37.3 us                                                          | 38.4 us: 1.03x slower                                                          |
| logging_format            | 7.11 us                                                          | 7.32 us: 1.03x slower                                                          |
| json                      | 5.35 ms                                                          | 5.51 ms: 1.03x slower                                                          |
| pidigits                  | 254 ms                                                           | 261 ms: 1.03x slower                                                           |
| genshi_xml                | 58.1 ms                                                          | 59.9 ms: 1.03x slower                                                          |
| logging_simple            | 6.40 us                                                          | 6.63 us: 1.04x slower                                                          |
| tornado_http              | 119 ms                                                           | 124 ms: 1.04x slower                                                           |
| deepcopy_reduce           | 3.39 us                                                          | 3.52 us: 1.04x slower                                                          |
| sqlglot_transpile         | 1.76 ms                                                          | 1.84 ms: 1.04x slower                                                          |
| async_tree_memoization_tg | 421 ms                                                           | 437 ms: 1.04x slower                                                           |
| pickle                    | 10.6 us                                                          | 11.0 us: 1.04x slower                                                          |
| pprint_pformat            | 1.66 sec                                                         | 1.73 sec: 1.04x slower                                                         |
| dask                      | 391 ms                                                           | 407 ms: 1.04x slower                                                           |
| 2to3                      | 291 ms                                                           | 306 ms: 1.05x slower                                                           |
| docutils                  | 2.98 sec                                                         | 3.13 sec: 1.05x slower                                                         |
| sympy_expand              | 501 ms                                                           | 526 ms: 1.05x slower                                                           |
| django_template           | 39.0 ms                                                          | 40.9 ms: 1.05x slower                                                          |
| sympy_str                 | 295 ms                                                           | 310 ms: 1.05x slower                                                           |
| meteor_contest            | 128 ms                                                           | 135 ms: 1.05x slower                                                           |
| sqlglot_normalize         | 120 ms                                                           | 127 ms: 1.06x slower                                                           |
| regex_effbot              | 3.40 ms                                                          | 3.60 ms: 1.06x slower                                                          |
| pycparser                 | 1.22 sec                                                         | 1.29 sec: 1.06x slower                                                         |
| sympy_sum                 | 155 ms                                                           | 165 ms: 1.06x slower                                                           |
| deepcopy                  | 377 us                                                           | 401 us: 1.06x slower                                                           |
| aiohttp                   | 1.07 ms                                                          | 1.15 ms: 1.07x slower                                                          |
| go                        | 165 ms                                                           | 177 ms: 1.07x slower                                                           |
| gunicorn                  | 1.04 ms                                                          | 1.12 ms: 1.07x slower                                                          |
| crypto_pyaes              | 73.6 ms                                                          | 79.1 ms: 1.08x slower                                                          |
| mdp                       | 2.46 sec                                                         | 2.65 sec: 1.08x slower                                                         |
| genshi_text               | 25.9 ms                                                          | 28.0 ms: 1.08x slower                                                          |
| async_generators          | 363 ms                                                           | 393 ms: 1.08x slower                                                           |
| fannkuch                  | 353 ms                                                           | 383 ms: 1.09x slower                                                           |
| sqlglot_optimize          | 59.5 ms                                                          | 64.7 ms: 1.09x slower                                                          |
| pyflate                   | 482 ms                                                           | 528 ms: 1.10x slower                                                           |
| nbody                     | 87.8 ms                                                          | 96.8 ms: 1.10x slower                                                          |
| mypy2                     | 764 ms                                                           | 852 ms: 1.11x slower                                                           |
| deltablue                 | 3.37 ms                                                          | 3.79 ms: 1.12x slower                                                          |
| sympy_integrate           | 23.2 ms                                                          | 26.1 ms: 1.12x slower                                                          |
| chaos                     | 59.6 ms                                                          | 69.0 ms: 1.16x slower                                                          |
| pathlib                   | 17.1 ms                                                          | 19.8 ms: 1.16x slower                                                          |
| scimark_monte_carlo       | 65.5 ms                                                          | 75.9 ms: 1.16x slower                                                          |
| comprehensions            | 17.0 us                                                          | 20.2 us: 1.19x slower                                                          |
| nqueens                   | 88.4 ms                                                          | 106 ms: 1.20x slower                                                           |
| raytrace                  | 260 ms                                                           | 316 ms: 1.21x slower                                                           |
| hexiom                    | 6.35 ms                                                          | 7.73 ms: 1.22x slower                                                          |
| scimark_lu                | 97.5 ms                                                          | 119 ms: 1.23x slower                                                           |
| bench_thread_pool         | 908 us                                                           | 1.13 ms: 1.25x slower                                                          |
| scimark_sor               | 119 ms                                                           | 156 ms: 1.31x slower                                                           |
| python_startup_no_site    | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                          |
| Geometric mean            | (ref)                                                            | 1.04x slower                                                                   |

Benchmark hidden because not significant (15): async_tree_memoization, async_tree_none, html5lib, async_tree_cpu_io_mixed, json_dumps, thrift, async_tree_none_tg, generators, asyncio_tcp_ssl, pickle_pure_python, async_tree_cpu_io_mixed_tg, scimark_fft, pylint, async_tree_io, bench_mp_pool
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.07x