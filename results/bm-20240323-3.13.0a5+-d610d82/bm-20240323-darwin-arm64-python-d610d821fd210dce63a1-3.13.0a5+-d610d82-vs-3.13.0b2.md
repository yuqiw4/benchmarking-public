# Results vs. 3.13.0b2

- fork: python
- ref: d610d821fd210dce63a1
- machine: darwin-arm64
- commit hash: d610d82
- commit date: 2024-03-23
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 164 ms: 1.02x slower                                                   |
| chameleon      | 4.27 ms                                                    | 4.46 ms: 1.05x slower                                                  |
| docutils       | 1.44 sec                                                   | 1.48 sec: 1.03x slower                                                 |
| html5lib       | 31.2 ms                                                    | 34.0 ms: 1.09x slower                                                  |
| tornado_http   | 66.7 ms                                                    | 81.6 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                      | 1.08x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed          | 467 ms                                                     | 455 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 354 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.02x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 130 ms: 1.03x slower                                                   |
| async_tree_none                  | 209 ms                                                     | 220 ms: 1.05x slower                                                   |
| async_tree_none_tg               | 198 ms                                                     | 208 ms: 1.05x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 64.3 ms: 1.07x slower                                                  |
| async_tree_eager_tg              | 41.4 ms                                                    | 44.6 ms: 1.08x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_eager_io, async_tree_io, async_tree_eager_io_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_eager_memoization, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| float          | 48.6 ms                                                    | 51.2 ms: 1.05x slower                                                  |
| nbody          | 59.6 ms                                                    | 71.0 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                      | 1.08x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 17.3 ms                                                    | 16.9 ms: 1.02x faster                                                  |
| regex_effbot   | 2.58 ms                                                    | 2.54 ms: 1.02x faster                                                  |
| regex_dna      | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| regex_compile  | 68.5 ms                                                    | 70.0 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 106 ms                                                     | 99.4 ms: 1.06x faster                                                  |
| pickle               | 7.48 us                                                    | 7.25 us: 1.03x faster                                                  |
| xml_etree_iterparse  | 71.5 ms                                                    | 69.6 ms: 1.03x faster                                                  |
| pickle_dict          | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| json_loads           | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| xml_etree_process    | 37.1 ms                                                    | 37.5 ms: 1.01x slower                                                  |
| json_dumps           | 6.23 ms                                                    | 6.36 ms: 1.02x slower                                                  |
| pickle_pure_python   | 179 us                                                     | 185 us: 1.04x slower                                                   |
| xml_etree_generate   | 52.7 ms                                                    | 54.6 ms: 1.04x slower                                                  |
| tomli_loads          | 1.47 sec                                                   | 1.52 sec: 1.04x slower                                                 |
| unpickle_pure_python | 141 us                                                     | 148 us: 1.05x slower                                                   |
| unpickle_list        | 2.88 us                                                    | 3.05 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (2): pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                    | 14.9 ms: 1.02x faster                                                  |
| python_startup_no_site | 12.3 ms                                                    | 13.0 ms: 1.06x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 7.06 ms: 1.01x slower                                                  |
| genshi_text     | 13.9 ms                                                    | 14.4 ms: 1.03x slower                                                  |
| genshi_xml      | 29.9 ms                                                    | 31.2 ms: 1.04x slower                                                  |
| django_template | 19.4 ms                                                    | 20.3 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| create_gc_cycles                 | 897 us                                                     | 712 us: 1.26x faster                                                   |
| typing_runtime_protocols         | 87.6 us                                                    | 69.7 us: 1.26x faster                                                  |
| xml_etree_parse                  | 106 ms                                                     | 99.4 ms: 1.06x faster                                                  |
| crypto_pyaes                     | 49.5 ms                                                    | 47.1 ms: 1.05x faster                                                  |
| bench_mp_pool                    | 47.2 ms                                                    | 45.1 ms: 1.05x faster                                                  |
| pickle                           | 7.48 us                                                    | 7.25 us: 1.03x faster                                                  |
| xml_etree_iterparse              | 71.5 ms                                                    | 69.6 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed          | 467 ms                                                     | 455 ms: 1.03x faster                                                   |
| gc_traversal                     | 2.45 ms                                                    | 2.39 ms: 1.02x faster                                                  |
| regex_v8                         | 17.3 ms                                                    | 16.9 ms: 1.02x faster                                                  |
| python_startup                   | 15.2 ms                                                    | 14.9 ms: 1.02x faster                                                  |
| regex_effbot                     | 2.58 ms                                                    | 2.54 ms: 1.02x faster                                                  |
| telco                            | 4.60 ms                                                    | 4.53 ms: 1.02x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 354 ms: 1.01x faster                                                   |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| mdp                              | 1.53 sec                                                   | 1.52 sec: 1.01x faster                                                 |
| sympy_integrate                  | 10.3 ms                                                    | 10.3 ms: 1.01x faster                                                  |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                   |
| pidigits                         | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| sqlite_synth                     | 1.55 us                                                    | 1.56 us: 1.00x slower                                                  |
| sympy_str                        | 131 ms                                                     | 132 ms: 1.01x slower                                                   |
| mako                             | 6.99 ms                                                    | 7.06 ms: 1.01x slower                                                  |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| xml_etree_process                | 37.1 ms                                                    | 37.5 ms: 1.01x slower                                                  |
| sympy_sum                        | 69.2 ms                                                    | 70.0 ms: 1.01x slower                                                  |
| meteor_contest                   | 70.3 ms                                                    | 71.2 ms: 1.01x slower                                                  |
| sympy_expand                     | 226 ms                                                     | 228 ms: 1.01x slower                                                   |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.31 sec: 1.01x slower                                                 |
| richards_super                   | 35.2 ms                                                    | 35.7 ms: 1.01x slower                                                  |
| thrift                           | 435 us                                                     | 442 us: 1.02x slower                                                   |
| regex_dna                        | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.02x slower                                                   |
| richards                         | 31.8 ms                                                    | 32.3 ms: 1.02x slower                                                  |
| deepcopy_reduce                  | 1.82 us                                                    | 1.86 us: 1.02x slower                                                  |
| async_generators                 | 281 ms                                                     | 286 ms: 1.02x slower                                                   |
| sqlglot_transpile                | 891 us                                                     | 909 us: 1.02x slower                                                   |
| json_dumps                       | 6.23 ms                                                    | 6.36 ms: 1.02x slower                                                  |
| regex_compile                    | 68.5 ms                                                    | 70.0 ms: 1.02x slower                                                  |
| 2to3                             | 161 ms                                                     | 164 ms: 1.02x slower                                                   |
| sqlglot_parse                    | 732 us                                                     | 748 us: 1.02x slower                                                   |
| scimark_lu                       | 66.9 ms                                                    | 68.5 ms: 1.02x slower                                                  |
| pyflate                          | 321 ms                                                     | 329 ms: 1.02x slower                                                   |
| pprint_pformat                   | 947 ms                                                     | 972 ms: 1.03x slower                                                   |
| pprint_safe_repr                 | 465 ms                                                     | 478 ms: 1.03x slower                                                   |
| sqlglot_optimize                 | 30.9 ms                                                    | 31.9 ms: 1.03x slower                                                  |
| sqlglot_normalize                | 166 ms                                                     | 171 ms: 1.03x slower                                                   |
| docutils                         | 1.44 sec                                                   | 1.48 sec: 1.03x slower                                                 |
| genshi_text                      | 13.9 ms                                                    | 14.4 ms: 1.03x slower                                                  |
| hexiom                           | 4.06 ms                                                    | 4.20 ms: 1.03x slower                                                  |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 130 ms: 1.03x slower                                                   |
| pickle_pure_python               | 179 us                                                     | 185 us: 1.04x slower                                                   |
| xml_etree_generate               | 52.7 ms                                                    | 54.6 ms: 1.04x slower                                                  |
| tomli_loads                      | 1.47 sec                                                   | 1.52 sec: 1.04x slower                                                 |
| dulwich_log                      | 27.6 ms                                                    | 28.6 ms: 1.04x slower                                                  |
| genshi_xml                       | 29.9 ms                                                    | 31.2 ms: 1.04x slower                                                  |
| deepcopy_memo                    | 22.6 us                                                    | 23.6 us: 1.04x slower                                                  |
| django_template                  | 19.4 ms                                                    | 20.3 ms: 1.04x slower                                                  |
| deepcopy                         | 204 us                                                     | 213 us: 1.04x slower                                                   |
| pycparser                        | 632 ms                                                     | 661 ms: 1.04x slower                                                   |
| chameleon                        | 4.27 ms                                                    | 4.46 ms: 1.05x slower                                                  |
| async_tree_none                  | 209 ms                                                     | 220 ms: 1.05x slower                                                   |
| coverage                         | 45.0 ms                                                    | 47.2 ms: 1.05x slower                                                  |
| scimark_monte_carlo              | 42.5 ms                                                    | 44.6 ms: 1.05x slower                                                  |
| unpickle_pure_python             | 141 us                                                     | 148 us: 1.05x slower                                                   |
| async_tree_none_tg               | 198 ms                                                     | 208 ms: 1.05x slower                                                   |
| float                            | 48.6 ms                                                    | 51.2 ms: 1.05x slower                                                  |
| unpickle_list                    | 2.88 us                                                    | 3.05 us: 1.06x slower                                                  |
| scimark_sor                      | 94.9 ms                                                    | 100 ms: 1.06x slower                                                   |
| python_startup_no_site           | 12.3 ms                                                    | 13.0 ms: 1.06x slower                                                  |
| deltablue                        | 2.14 ms                                                    | 2.27 ms: 1.06x slower                                                  |
| pathlib                          | 23.3 ms                                                    | 24.7 ms: 1.06x slower                                                  |
| raytrace                         | 147 ms                                                     | 156 ms: 1.06x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 64.3 ms: 1.07x slower                                                  |
| bench_thread_pool                | 447 us                                                     | 477 us: 1.07x slower                                                   |
| aiohttp                          | 997 us                                                     | 1.07 ms: 1.07x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 55.9 ms: 1.07x slower                                                  |
| fannkuch                         | 248 ms                                                     | 266 ms: 1.07x slower                                                   |
| logging_format                   | 3.31 us                                                    | 3.55 us: 1.07x slower                                                  |
| spectral_norm                    | 66.4 ms                                                    | 71.3 ms: 1.07x slower                                                  |
| async_tree_eager_tg              | 41.4 ms                                                    | 44.6 ms: 1.08x slower                                                  |
| logging_simple                   | 3.04 us                                                    | 3.29 us: 1.08x slower                                                  |
| logging_silent                   | 60.1 ns                                                    | 65.1 ns: 1.08x slower                                                  |
| chaos                            | 34.0 ms                                                    | 36.9 ms: 1.09x slower                                                  |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.02 ms: 1.09x slower                                                  |
| html5lib                         | 31.2 ms                                                    | 34.0 ms: 1.09x slower                                                  |
| scimark_fft                      | 181 ms                                                     | 197 ms: 1.09x slower                                                   |
| coroutines                       | 15.8 ms                                                    | 17.3 ms: 1.09x slower                                                  |
| comprehensions                   | 10.2 us                                                    | 11.2 us: 1.10x slower                                                  |
| generators                       | 22.9 ms                                                    | 27.1 ms: 1.18x slower                                                  |
| nbody                            | 59.6 ms                                                    | 71.0 ms: 1.19x slower                                                  |
| tornado_http                     | 66.7 ms                                                    | 81.6 ms: 1.22x slower                                                  |
| mypy2                            | 379 ms                                                     | 466 ms: 1.23x slower                                                   |
| Geometric mean                   | (ref)                                                      | 1.03x slower                                                           |

Benchmark hidden because not significant (16): async_tree_memoization, async_tree_eager_io, pylint, asyncio_tcp, async_tree_io, async_tree_eager_io_tg, pickle_list, dask, async_tree_cpu_io_mixed_tg, json, go, unpickle, async_tree_memoization_tg, async_tree_eager_memoization, async_tree_io_tg, gunicorn
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240323-3.13.0a5+-d610d82/bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.96x