# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 303 ms: 1.04x slower                                                       |
| chameleon      | 7.40 ms                                                          | 7.52 ms: 1.02x slower                                                      |
| docutils       | 2.98 sec                                                         | 3.11 sec: 1.04x slower                                                     |
| html5lib       | 74.7 ms                                                          | 74.2 ms: 1.01x faster                                                      |
| tornado_http   | 119 ms                                                           | 124 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                            | 1.03x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|---------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg          | 900 ms                                                           | 912 ms: 1.01x slower                                                       |
| async_tree_memoization_tg | 421 ms                                                           | 443 ms: 1.05x slower                                                       |
| Geometric mean            | (ref)                                                            | 1.01x slower                                                               |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 78.6 ms: 1.02x faster                                                      |
| pidigits       | 254 ms                                                           | 262 ms: 1.03x slower                                                       |
| nbody          | 87.8 ms                                                          | 103 ms: 1.17x slower                                                       |
| Geometric mean | (ref)                                                            | 1.06x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 245 ms: 1.02x faster                                                       |
| regex_v8       | 26.0 ms                                                          | 25.8 ms: 1.01x faster                                                      |
| regex_compile  | 144 ms                                                           | 151 ms: 1.05x slower                                                       |
| regex_effbot   | 3.40 ms                                                          | 3.69 ms: 1.09x slower                                                      |
| Geometric mean | (ref)                                                            | 1.02x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_dict          | 32.8 us                                                          | 30.7 us: 1.07x faster                                                      |
| unpickle             | 15.7 us                                                          | 14.8 us: 1.06x faster                                                      |
| unpickle_list        | 4.70 us                                                          | 4.56 us: 1.03x faster                                                      |
| pickle               | 10.6 us                                                          | 10.4 us: 1.02x faster                                                      |
| tomli_loads          | 2.40 sec                                                         | 2.36 sec: 1.02x faster                                                     |
| xml_etree_process    | 59.7 ms                                                          | 58.9 ms: 1.01x faster                                                      |
| json_dumps           | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                      |
| xml_etree_generate   | 85.7 ms                                                          | 86.0 ms: 1.00x slower                                                      |
| xml_etree_parse      | 144 ms                                                           | 144 ms: 1.00x slower                                                       |
| pickle_list          | 4.44 us                                                          | 4.49 us: 1.01x slower                                                      |
| pickle_pure_python   | 307 us                                                           | 313 us: 1.02x slower                                                       |
| json_loads           | 25.0 us                                                          | 25.6 us: 1.02x slower                                                      |
| xml_etree_iterparse  | 103 ms                                                           | 105 ms: 1.03x slower                                                       |
| unpickle_pure_python | 224 us                                                           | 244 us: 1.09x slower                                                       |
| Geometric mean       | (ref)                                                            | 1.00x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                      |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                      |
| Geometric mean         | (ref)                                                            | 1.17x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 10.2 ms: 1.01x faster                                                      |
| genshi_xml      | 58.1 ms                                                          | 58.6 ms: 1.01x slower                                                      |
| django_template | 39.0 ms                                                          | 39.7 ms: 1.02x slower                                                      |
| genshi_text     | 25.9 ms                                                          | 26.6 ms: 1.02x slower                                                      |
| Geometric mean  | (ref)                                                            | 1.01x slower                                                               |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|---------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols  | 171 us                                                           | 119 us: 1.43x faster                                                       |
| create_gc_cycles          | 2.00 ms                                                          | 1.80 ms: 1.11x faster                                                      |
| gc_traversal              | 4.69 ms                                                          | 4.36 ms: 1.08x faster                                                      |
| pickle_dict               | 32.8 us                                                          | 30.7 us: 1.07x faster                                                      |
| unpickle                  | 15.7 us                                                          | 14.8 us: 1.06x faster                                                      |
| coverage                  | 83.5 ms                                                          | 80.3 ms: 1.04x faster                                                      |
| telco                     | 8.40 ms                                                          | 8.10 ms: 1.04x faster                                                      |
| unpickle_list             | 4.70 us                                                          | 4.56 us: 1.03x faster                                                      |
| thrift                    | 880 us                                                           | 861 us: 1.02x faster                                                       |
| sqlite_synth              | 2.80 us                                                          | 2.74 us: 1.02x faster                                                      |
| float                     | 80.2 ms                                                          | 78.6 ms: 1.02x faster                                                      |
| regex_dna                 | 249 ms                                                           | 245 ms: 1.02x faster                                                       |
| pickle                    | 10.6 us                                                          | 10.4 us: 1.02x faster                                                      |
| tomli_loads               | 2.40 sec                                                         | 2.36 sec: 1.02x faster                                                     |
| richards_super            | 61.2 ms                                                          | 60.2 ms: 1.02x faster                                                      |
| asyncio_tcp               | 378 ms                                                           | 372 ms: 1.01x faster                                                       |
| xml_etree_process         | 59.7 ms                                                          | 58.9 ms: 1.01x faster                                                      |
| mako                      | 10.4 ms                                                          | 10.2 ms: 1.01x faster                                                      |
| generators                | 33.5 ms                                                          | 33.1 ms: 1.01x faster                                                      |
| regex_v8                  | 26.0 ms                                                          | 25.8 ms: 1.01x faster                                                      |
| html5lib                  | 74.7 ms                                                          | 74.2 ms: 1.01x faster                                                      |
| json_dumps                | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                      |
| xml_etree_generate        | 85.7 ms                                                          | 86.0 ms: 1.00x slower                                                      |
| sqlglot_normalize         | 120 ms                                                           | 121 ms: 1.00x slower                                                       |
| richards                  | 53.4 ms                                                          | 53.7 ms: 1.00x slower                                                      |
| xml_etree_parse           | 144 ms                                                           | 144 ms: 1.00x slower                                                       |
| sympy_expand              | 501 ms                                                           | 505 ms: 1.01x slower                                                       |
| json                      | 5.35 ms                                                          | 5.40 ms: 1.01x slower                                                      |
| genshi_xml                | 58.1 ms                                                          | 58.6 ms: 1.01x slower                                                      |
| pickle_list               | 4.44 us                                                          | 4.49 us: 1.01x slower                                                      |
| async_tree_io_tg          | 900 ms                                                           | 912 ms: 1.01x slower                                                       |
| chameleon                 | 7.40 ms                                                          | 7.52 ms: 1.02x slower                                                      |
| pickle_pure_python        | 307 us                                                           | 313 us: 1.02x slower                                                       |
| spectral_norm             | 97.3 ms                                                          | 99.0 ms: 1.02x slower                                                      |
| django_template           | 39.0 ms                                                          | 39.7 ms: 1.02x slower                                                      |
| json_loads                | 25.0 us                                                          | 25.6 us: 1.02x slower                                                      |
| coroutines                | 22.0 ms                                                          | 22.5 ms: 1.02x slower                                                      |
| sqlglot_parse             | 1.39 ms                                                          | 1.42 ms: 1.02x slower                                                      |
| python_startup            | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                      |
| sympy_str                 | 295 ms                                                           | 302 ms: 1.02x slower                                                       |
| genshi_text               | 25.9 ms                                                          | 26.6 ms: 1.02x slower                                                      |
| xml_etree_iterparse       | 103 ms                                                           | 105 ms: 1.03x slower                                                       |
| logging_silent            | 96.3 ns                                                          | 99.0 ns: 1.03x slower                                                      |
| pycparser                 | 1.22 sec                                                         | 1.26 sec: 1.03x slower                                                     |
| dulwich_log               | 67.3 ms                                                          | 69.4 ms: 1.03x slower                                                      |
| pidigits                  | 254 ms                                                           | 262 ms: 1.03x slower                                                       |
| deepcopy_memo             | 37.3 us                                                          | 38.5 us: 1.03x slower                                                      |
| sqlglot_transpile         | 1.76 ms                                                          | 1.83 ms: 1.04x slower                                                      |
| tornado_http              | 119 ms                                                           | 124 ms: 1.04x slower                                                       |
| logging_format            | 7.11 us                                                          | 7.38 us: 1.04x slower                                                      |
| dask                      | 391 ms                                                           | 406 ms: 1.04x slower                                                       |
| 2to3                      | 291 ms                                                           | 303 ms: 1.04x slower                                                       |
| docutils                  | 2.98 sec                                                         | 3.11 sec: 1.04x slower                                                     |
| regex_compile             | 144 ms                                                           | 151 ms: 1.05x slower                                                       |
| deepcopy                  | 377 us                                                           | 395 us: 1.05x slower                                                       |
| sympy_sum                 | 155 ms                                                           | 162 ms: 1.05x slower                                                       |
| gunicorn                  | 1.04 ms                                                          | 1.09 ms: 1.05x slower                                                      |
| meteor_contest            | 128 ms                                                           | 134 ms: 1.05x slower                                                       |
| aiohttp                   | 1.07 ms                                                          | 1.13 ms: 1.05x slower                                                      |
| logging_simple            | 6.40 us                                                          | 6.73 us: 1.05x slower                                                      |
| scimark_sparse_mat_mult   | 4.28 ms                                                          | 4.50 ms: 1.05x slower                                                      |
| async_tree_memoization_tg | 421 ms                                                           | 443 ms: 1.05x slower                                                       |
| sqlglot_optimize          | 59.5 ms                                                          | 62.9 ms: 1.06x slower                                                      |
| async_generators          | 363 ms                                                           | 389 ms: 1.07x slower                                                       |
| mdp                       | 2.46 sec                                                         | 2.65 sec: 1.08x slower                                                     |
| pprint_pformat            | 1.66 sec                                                         | 1.79 sec: 1.08x slower                                                     |
| pyflate                   | 482 ms                                                           | 522 ms: 1.08x slower                                                       |
| regex_effbot              | 3.40 ms                                                          | 3.69 ms: 1.09x slower                                                      |
| mypy2                     | 764 ms                                                           | 831 ms: 1.09x slower                                                       |
| unpickle_pure_python      | 224 us                                                           | 244 us: 1.09x slower                                                       |
| scimark_fft               | 312 ms                                                           | 341 ms: 1.09x slower                                                       |
| sympy_integrate           | 23.2 ms                                                          | 25.4 ms: 1.09x slower                                                      |
| crypto_pyaes              | 73.6 ms                                                          | 81.1 ms: 1.10x slower                                                      |
| go                        | 165 ms                                                           | 182 ms: 1.10x slower                                                       |
| pprint_safe_repr          | 818 ms                                                           | 902 ms: 1.10x slower                                                       |
| pathlib                   | 17.1 ms                                                          | 19.2 ms: 1.12x slower                                                      |
| deltablue                 | 3.37 ms                                                          | 3.80 ms: 1.12x slower                                                      |
| fannkuch                  | 353 ms                                                           | 408 ms: 1.16x slower                                                       |
| nbody                     | 87.8 ms                                                          | 103 ms: 1.17x slower                                                       |
| chaos                     | 59.6 ms                                                          | 69.8 ms: 1.17x slower                                                      |
| raytrace                  | 260 ms                                                           | 306 ms: 1.17x slower                                                       |
| scimark_monte_carlo       | 65.5 ms                                                          | 77.9 ms: 1.19x slower                                                      |
| comprehensions            | 17.0 us                                                          | 20.4 us: 1.20x slower                                                      |
| nqueens                   | 88.4 ms                                                          | 109 ms: 1.23x slower                                                       |
| bench_thread_pool         | 908 us                                                           | 1.12 ms: 1.23x slower                                                      |
| hexiom                    | 6.35 ms                                                          | 8.00 ms: 1.26x slower                                                      |
| python_startup_no_site    | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                      |
| scimark_lu                | 97.5 ms                                                          | 130 ms: 1.33x slower                                                       |
| scimark_sor               | 119 ms                                                           | 160 ms: 1.35x slower                                                       |
| Geometric mean            | (ref)                                                            | 1.04x slower                                                               |

Benchmark hidden because not significant (11): async_tree_memoization, async_tree_none, asyncio_websockets, async_tree_cpu_io_mixed, deepcopy_reduce, asyncio_tcp_ssl, pylint, async_tree_none_tg, bench_mp_pool, async_tree_cpu_io_mixed_tg, async_tree_io
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.06x