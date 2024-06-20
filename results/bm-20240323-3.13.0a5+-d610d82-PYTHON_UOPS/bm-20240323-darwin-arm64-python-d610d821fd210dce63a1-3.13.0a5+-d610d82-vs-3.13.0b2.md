# Results vs. 3.13.0b2

- fork: python
- ref: d610d821fd210dce63a1
- machine: darwin-arm64
- commit hash: d610d82
- commit date: 2024-03-23
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 177 ms: 1.10x slower                                                   |
| chameleon      | 4.27 ms                                                    | 4.71 ms: 1.10x slower                                                  |
| docutils       | 1.44 sec                                                   | 1.60 sec: 1.11x slower                                                 |
| html5lib       | 31.2 ms                                                    | 35.0 ms: 1.12x slower                                                  |
| tornado_http   | 66.7 ms                                                    | 81.6 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                      | 1.13x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 360 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 339 ms: 1.03x slower                                                   |
| async_tree_io                    | 563 ms                                                     | 583 ms: 1.04x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.04x slower                                                   |
| async_tree_io_tg                 | 565 ms                                                     | 591 ms: 1.05x slower                                                   |
| async_tree_eager_memoization     | 152 ms                                                     | 160 ms: 1.05x slower                                                   |
| async_tree_memoization_tg        | 240 ms                                                     | 260 ms: 1.09x slower                                                   |
| async_tree_none_tg               | 198 ms                                                     | 216 ms: 1.09x slower                                                   |
| async_tree_none                  | 209 ms                                                     | 230 ms: 1.10x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 47.0 ms: 1.14x slower                                                  |
| async_tree_eager                 | 60.3 ms                                                    | 71.0 ms: 1.18x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.05x slower                                                           |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed, async_tree_eager_io, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_eager_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| float          | 48.6 ms                                                    | 66.6 ms: 1.37x slower                                                  |
| nbody          | 59.6 ms                                                    | 86.0 ms: 1.44x slower                                                  |
| Geometric mean | (ref)                                                      | 1.26x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.58 ms                                                    | 2.55 ms: 1.01x faster                                                  |
| regex_v8       | 17.3 ms                                                    | 17.2 ms: 1.01x faster                                                  |
| regex_dna      | 149 ms                                                     | 151 ms: 1.01x slower                                                   |
| regex_compile  | 68.5 ms                                                    | 95.0 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                      | 1.08x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 106 ms                                                     | 98.9 ms: 1.07x faster                                                  |
| pickle               | 7.48 us                                                    | 7.25 us: 1.03x faster                                                  |
| pickle_dict          | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| json_loads           | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| json_dumps           | 6.23 ms                                                    | 6.48 ms: 1.04x slower                                                  |
| xml_etree_iterparse  | 71.5 ms                                                    | 75.2 ms: 1.05x slower                                                  |
| pickle_pure_python   | 179 us                                                     | 190 us: 1.06x slower                                                   |
| unpickle_list        | 2.88 us                                                    | 3.07 us: 1.06x slower                                                  |
| xml_etree_process    | 37.1 ms                                                    | 39.8 ms: 1.08x slower                                                  |
| xml_etree_generate   | 52.7 ms                                                    | 57.9 ms: 1.10x slower                                                  |
| tomli_loads          | 1.47 sec                                                   | 1.68 sec: 1.15x slower                                                 |
| unpickle_pure_python | 141 us                                                     | 186 us: 1.32x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.05x slower                                                           |

Benchmark hidden because not significant (2): unpickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                    | 14.8 ms: 1.03x faster                                                  |
| python_startup_no_site | 12.3 ms                                                    | 13.0 ms: 1.06x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 29.9 ms                                                    | 34.5 ms: 1.15x slower                                                  |
| django_template | 19.4 ms                                                    | 22.4 ms: 1.15x slower                                                  |
| genshi_text     | 13.9 ms                                                    | 16.5 ms: 1.18x slower                                                  |
| mako            | 6.99 ms                                                    | 9.45 ms: 1.35x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.21x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| create_gc_cycles                 | 897 us                                                     | 718 us: 1.25x faster                                                   |
| typing_runtime_protocols         | 87.6 us                                                    | 72.4 us: 1.21x faster                                                  |
| xml_etree_parse                  | 106 ms                                                     | 98.9 ms: 1.07x faster                                                  |
| pickle                           | 7.48 us                                                    | 7.25 us: 1.03x faster                                                  |
| python_startup                   | 15.2 ms                                                    | 14.8 ms: 1.03x faster                                                  |
| bench_mp_pool                    | 47.2 ms                                                    | 46.0 ms: 1.02x faster                                                  |
| gc_traversal                     | 2.45 ms                                                    | 2.40 ms: 1.02x faster                                                  |
| regex_effbot                     | 2.58 ms                                                    | 2.55 ms: 1.01x faster                                                  |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| regex_v8                         | 17.3 ms                                                    | 17.2 ms: 1.01x faster                                                  |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                   |
| pidigits                         | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 360 ms: 1.01x slower                                                   |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| json                             | 2.93 ms                                                    | 2.96 ms: 1.01x slower                                                  |
| thrift                           | 435 us                                                     | 441 us: 1.01x slower                                                   |
| regex_dna                        | 149 ms                                                     | 151 ms: 1.01x slower                                                   |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.31 sec: 1.02x slower                                                 |
| dask                             | 221 ms                                                     | 226 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 339 ms: 1.03x slower                                                   |
| async_tree_io                    | 563 ms                                                     | 583 ms: 1.04x slower                                                   |
| telco                            | 4.60 ms                                                    | 4.78 ms: 1.04x slower                                                  |
| json_dumps                       | 6.23 ms                                                    | 6.48 ms: 1.04x slower                                                  |
| coverage                         | 45.0 ms                                                    | 47.0 ms: 1.04x slower                                                  |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.04x slower                                                   |
| async_tree_io_tg                 | 565 ms                                                     | 591 ms: 1.05x slower                                                   |
| async_tree_eager_memoization     | 152 ms                                                     | 160 ms: 1.05x slower                                                   |
| sqlite_synth                     | 1.55 us                                                    | 1.63 us: 1.05x slower                                                  |
| xml_etree_iterparse              | 71.5 ms                                                    | 75.2 ms: 1.05x slower                                                  |
| pathlib                          | 23.3 ms                                                    | 24.6 ms: 1.05x slower                                                  |
| deepcopy_reduce                  | 1.82 us                                                    | 1.92 us: 1.06x slower                                                  |
| mdp                              | 1.53 sec                                                   | 1.62 sec: 1.06x slower                                                 |
| python_startup_no_site           | 12.3 ms                                                    | 13.0 ms: 1.06x slower                                                  |
| pickle_pure_python               | 179 us                                                     | 190 us: 1.06x slower                                                   |
| unpickle_list                    | 2.88 us                                                    | 3.07 us: 1.06x slower                                                  |
| async_generators                 | 281 ms                                                     | 299 ms: 1.06x slower                                                   |
| xml_etree_process                | 37.1 ms                                                    | 39.8 ms: 1.08x slower                                                  |
| dulwich_log                      | 27.6 ms                                                    | 29.8 ms: 1.08x slower                                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 260 ms: 1.09x slower                                                   |
| sympy_expand                     | 226 ms                                                     | 246 ms: 1.09x slower                                                   |
| async_tree_none_tg               | 198 ms                                                     | 216 ms: 1.09x slower                                                   |
| deepcopy                         | 204 us                                                     | 223 us: 1.09x slower                                                   |
| 2to3                             | 161 ms                                                     | 177 ms: 1.10x slower                                                   |
| xml_etree_generate               | 52.7 ms                                                    | 57.9 ms: 1.10x slower                                                  |
| async_tree_none                  | 209 ms                                                     | 230 ms: 1.10x slower                                                   |
| chameleon                        | 4.27 ms                                                    | 4.71 ms: 1.10x slower                                                  |
| sqlglot_transpile                | 891 us                                                     | 988 us: 1.11x slower                                                   |
| coroutines                       | 15.8 ms                                                    | 17.6 ms: 1.11x slower                                                  |
| pycparser                        | 632 ms                                                     | 702 ms: 1.11x slower                                                   |
| docutils                         | 1.44 sec                                                   | 1.60 sec: 1.11x slower                                                 |
| richards_super                   | 35.2 ms                                                    | 39.2 ms: 1.11x slower                                                  |
| logging_format                   | 3.31 us                                                    | 3.69 us: 1.12x slower                                                  |
| sqlglot_parse                    | 732 us                                                     | 819 us: 1.12x slower                                                   |
| html5lib                         | 31.2 ms                                                    | 35.0 ms: 1.12x slower                                                  |
| logging_simple                   | 3.04 us                                                    | 3.41 us: 1.12x slower                                                  |
| aiohttp                          | 997 us                                                     | 1.12 ms: 1.13x slower                                                  |
| richards                         | 31.8 ms                                                    | 36.0 ms: 1.13x slower                                                  |
| gunicorn                         | 1.04 ms                                                    | 1.17 ms: 1.13x slower                                                  |
| sqlglot_normalize                | 166 ms                                                     | 188 ms: 1.13x slower                                                   |
| logging_silent                   | 60.1 ns                                                    | 68.2 ns: 1.13x slower                                                  |
| bench_thread_pool                | 447 us                                                     | 508 us: 1.14x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 47.0 ms: 1.14x slower                                                  |
| sympy_integrate                  | 10.3 ms                                                    | 11.8 ms: 1.14x slower                                                  |
| tomli_loads                      | 1.47 sec                                                   | 1.68 sec: 1.15x slower                                                 |
| crypto_pyaes                     | 49.5 ms                                                    | 56.8 ms: 1.15x slower                                                  |
| sympy_str                        | 131 ms                                                     | 151 ms: 1.15x slower                                                   |
| genshi_xml                       | 29.9 ms                                                    | 34.5 ms: 1.15x slower                                                  |
| go                               | 101 ms                                                     | 116 ms: 1.15x slower                                                   |
| django_template                  | 19.4 ms                                                    | 22.4 ms: 1.15x slower                                                  |
| meteor_contest                   | 70.3 ms                                                    | 81.3 ms: 1.16x slower                                                  |
| sqlglot_optimize                 | 30.9 ms                                                    | 36.0 ms: 1.17x slower                                                  |
| sympy_sum                        | 69.2 ms                                                    | 80.9 ms: 1.17x slower                                                  |
| async_tree_eager                 | 60.3 ms                                                    | 71.0 ms: 1.18x slower                                                  |
| genshi_text                      | 13.9 ms                                                    | 16.5 ms: 1.18x slower                                                  |
| scimark_sor                      | 94.9 ms                                                    | 113 ms: 1.20x slower                                                   |
| generators                       | 22.9 ms                                                    | 27.4 ms: 1.20x slower                                                  |
| deltablue                        | 2.14 ms                                                    | 2.60 ms: 1.22x slower                                                  |
| tornado_http                     | 66.7 ms                                                    | 81.6 ms: 1.22x slower                                                  |
| deepcopy_memo                    | 22.6 us                                                    | 27.7 us: 1.23x slower                                                  |
| pprint_safe_repr                 | 465 ms                                                     | 588 ms: 1.27x slower                                                   |
| pprint_pformat                   | 947 ms                                                     | 1.20 sec: 1.27x slower                                                 |
| pyflate                          | 321 ms                                                     | 409 ms: 1.28x slower                                                   |
| mypy2                            | 379 ms                                                     | 495 ms: 1.31x slower                                                   |
| chaos                            | 34.0 ms                                                    | 45.0 ms: 1.32x slower                                                  |
| unpickle_pure_python             | 141 us                                                     | 186 us: 1.32x slower                                                   |
| mako                             | 6.99 ms                                                    | 9.45 ms: 1.35x slower                                                  |
| scimark_fft                      | 181 ms                                                     | 245 ms: 1.35x slower                                                   |
| raytrace                         | 147 ms                                                     | 200 ms: 1.36x slower                                                   |
| float                            | 48.6 ms                                                    | 66.6 ms: 1.37x slower                                                  |
| regex_compile                    | 68.5 ms                                                    | 95.0 ms: 1.39x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 73.1 ms: 1.40x slower                                                  |
| fannkuch                         | 248 ms                                                     | 349 ms: 1.40x slower                                                   |
| scimark_monte_carlo              | 42.5 ms                                                    | 60.6 ms: 1.43x slower                                                  |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.98 ms: 1.43x slower                                                  |
| nbody                            | 59.6 ms                                                    | 86.0 ms: 1.44x slower                                                  |
| scimark_lu                       | 66.9 ms                                                    | 99.8 ms: 1.49x slower                                                  |
| hexiom                           | 4.06 ms                                                    | 6.15 ms: 1.52x slower                                                  |
| spectral_norm                    | 66.4 ms                                                    | 103 ms: 1.55x slower                                                   |
| comprehensions                   | 10.2 us                                                    | 16.0 us: 1.58x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.12x slower                                                           |

Benchmark hidden because not significant (9): async_tree_cpu_io_mixed, unpickle, async_tree_eager_io, pickle_list, async_tree_cpu_io_mixed_tg, async_tree_memoization, asyncio_tcp, async_tree_eager_io_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240323-3.13.0a5+-d610d82-PYTHON_UOPS/bm-20240323-darwin-arm64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 0.97x