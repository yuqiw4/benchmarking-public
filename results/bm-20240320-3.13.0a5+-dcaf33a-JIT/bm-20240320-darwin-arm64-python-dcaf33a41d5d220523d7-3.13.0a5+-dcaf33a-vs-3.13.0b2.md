# Results vs. 3.13.0b2

- fork: python
- ref: dcaf33a41d5d220523d7
- machine: darwin-arm64
- commit hash: dcaf33a
- commit date: 2024-03-20
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 192 ms: 1.20x slower                                                   |
| chameleon      | 4.27 ms                                                    | 4.46 ms: 1.05x slower                                                  |
| docutils       | 1.44 sec                                                   | 2.60 sec: 1.81x slower                                                 |
| html5lib       | 31.2 ms                                                    | 38.1 ms: 1.22x slower                                                  |
| tornado_http   | 66.7 ms                                                    | 83.9 ms: 1.26x slower                                                  |
| Geometric mean | (ref)                                                      | 1.28x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_tg              | 41.4 ms                                                    | 44.6 ms: 1.08x slower                                                  |
| async_tree_eager                 | 60.3 ms                                                    | 65.3 ms: 1.08x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 407 ms: 1.23x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 515 ms: 1.44x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 331 ms: 2.64x slower                                                   |
| async_tree_eager_memoization     | 152 ms                                                     | 647 ms: 4.25x slower                                                   |
| async_tree_cpu_io_mixed          | 467 ms                                                     | 2.80 sec: 5.98x slower                                                 |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 2.96 sec: 6.56x slower                                                 |
| async_tree_none                  | 209 ms                                                     | 2.21 sec: 10.55x slower                                                |
| async_tree_memoization           | 260 ms                                                     | 2.82 sec: 10.88x slower                                                |
| async_tree_none_tg               | 198 ms                                                     | 2.44 sec: 12.35x slower                                                |
| async_tree_memoization_tg        | 240 ms                                                     | 2.96 sec: 12.37x slower                                                |
| async_tree_io                    | 563 ms                                                     | 8.92 sec: 15.83x slower                                                |
| async_tree_io_tg                 | 565 ms                                                     | 9.35 sec: 16.56x slower                                                |
| async_tree_eager_io              | 766 ms                                                     | 16.9 sec: 22.08x slower                                                |
| async_tree_eager_io_tg           | 768 ms                                                     | 18.0 sec: 23.40x slower                                                |
| Geometric mean                   | (ref)                                                      | 5.90x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| nbody          | 59.6 ms                                                    | 70.3 ms: 1.18x slower                                                  |
| float          | 48.6 ms                                                    | 89.5 ms: 1.84x slower                                                  |
| Geometric mean | (ref)                                                      | 1.30x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 17.3 ms                                                    | 17.1 ms: 1.01x faster                                                  |
| regex_dna      | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| regex_effbot   | 2.58 ms                                                    | 2.64 ms: 1.02x slower                                                  |
| regex_compile  | 68.5 ms                                                    | 82.0 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                      | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 1.47 sec                                                   | 1.31 sec: 1.12x faster                                                 |
| pickle_dict          | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| pickle               | 7.48 us                                                    | 7.44 us: 1.01x faster                                                  |
| json_loads           | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| unpickle_pure_python | 141 us                                                     | 142 us: 1.01x slower                                                   |
| json_dumps           | 6.23 ms                                                    | 6.39 ms: 1.03x slower                                                  |
| pickle_pure_python   | 179 us                                                     | 184 us: 1.03x slower                                                   |
| unpickle_list        | 2.88 us                                                    | 3.05 us: 1.06x slower                                                  |
| xml_etree_process    | 37.1 ms                                                    | 41.1 ms: 1.11x slower                                                  |
| xml_etree_generate   | 52.7 ms                                                    | 60.2 ms: 1.14x slower                                                  |
| xml_etree_parse      | 106 ms                                                     | 132 ms: 1.25x slower                                                   |
| xml_etree_iterparse  | 71.5 ms                                                    | 106 ms: 1.48x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.06x slower                                                           |

Benchmark hidden because not significant (2): unpickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                    | 17.8 ms: 1.17x slower                                                  |
| python_startup_no_site | 12.3 ms                                                    | 16.1 ms: 1.31x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 6.90 ms: 1.01x faster                                                  |
| django_template | 19.4 ms                                                    | 20.5 ms: 1.05x slower                                                  |
| genshi_text     | 13.9 ms                                                    | 14.7 ms: 1.06x slower                                                  |
| genshi_xml      | 29.9 ms                                                    | 35.7 ms: 1.19x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.07x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols         | 87.6 us                                                    | 69.6 us: 1.26x faster                                                  |
| create_gc_cycles                 | 897 us                                                     | 749 us: 1.20x faster                                                   |
| tomli_loads                      | 1.47 sec                                                   | 1.31 sec: 1.12x faster                                                 |
| crypto_pyaes                     | 49.5 ms                                                    | 47.0 ms: 1.05x faster                                                  |
| mako                             | 6.99 ms                                                    | 6.90 ms: 1.01x faster                                                  |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| regex_v8                         | 17.3 ms                                                    | 17.1 ms: 1.01x faster                                                  |
| telco                            | 4.60 ms                                                    | 4.57 ms: 1.01x faster                                                  |
| gc_traversal                     | 2.45 ms                                                    | 2.43 ms: 1.01x faster                                                  |
| richards_super                   | 35.2 ms                                                    | 35.0 ms: 1.01x faster                                                  |
| thrift                           | 435 us                                                     | 433 us: 1.01x faster                                                   |
| richards                         | 31.8 ms                                                    | 31.7 ms: 1.01x faster                                                  |
| pickle                           | 7.48 us                                                    | 7.44 us: 1.01x faster                                                  |
| asyncio_websockets               | 409 ms                                                     | 409 ms: 1.00x faster                                                   |
| pidigits                         | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| unpickle_pure_python             | 141 us                                                     | 142 us: 1.01x slower                                                   |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.31 sec: 1.02x slower                                                 |
| regex_dna                        | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| regex_effbot                     | 2.58 ms                                                    | 2.64 ms: 1.02x slower                                                  |
| sqlite_synth                     | 1.55 us                                                    | 1.59 us: 1.02x slower                                                  |
| deepcopy_reduce                  | 1.82 us                                                    | 1.86 us: 1.02x slower                                                  |
| json_dumps                       | 6.23 ms                                                    | 6.39 ms: 1.03x slower                                                  |
| pyflate                          | 321 ms                                                     | 330 ms: 1.03x slower                                                   |
| pickle_pure_python               | 179 us                                                     | 184 us: 1.03x slower                                                   |
| mdp                              | 1.53 sec                                                   | 1.60 sec: 1.04x slower                                                 |
| sympy_expand                     | 226 ms                                                     | 236 ms: 1.04x slower                                                   |
| deepcopy                         | 204 us                                                     | 213 us: 1.04x slower                                                   |
| chameleon                        | 4.27 ms                                                    | 4.46 ms: 1.05x slower                                                  |
| go                               | 101 ms                                                     | 105 ms: 1.05x slower                                                   |
| coverage                         | 45.0 ms                                                    | 47.2 ms: 1.05x slower                                                  |
| sympy_str                        | 131 ms                                                     | 138 ms: 1.05x slower                                                   |
| meteor_contest                   | 70.3 ms                                                    | 73.9 ms: 1.05x slower                                                  |
| scimark_monte_carlo              | 42.5 ms                                                    | 44.7 ms: 1.05x slower                                                  |
| sqlglot_normalize                | 166 ms                                                     | 174 ms: 1.05x slower                                                   |
| fannkuch                         | 248 ms                                                     | 261 ms: 1.05x slower                                                   |
| django_template                  | 19.4 ms                                                    | 20.5 ms: 1.05x slower                                                  |
| unpickle_list                    | 2.88 us                                                    | 3.05 us: 1.06x slower                                                  |
| genshi_text                      | 13.9 ms                                                    | 14.7 ms: 1.06x slower                                                  |
| pathlib                          | 23.3 ms                                                    | 24.7 ms: 1.06x slower                                                  |
| pprint_safe_repr                 | 465 ms                                                     | 492 ms: 1.06x slower                                                   |
| sympy_integrate                  | 10.3 ms                                                    | 11.0 ms: 1.06x slower                                                  |
| async_tree_eager_tg              | 41.4 ms                                                    | 44.6 ms: 1.08x slower                                                  |
| deepcopy_memo                    | 22.6 us                                                    | 24.4 us: 1.08x slower                                                  |
| pprint_pformat                   | 947 ms                                                     | 1.02 sec: 1.08x slower                                                 |
| dulwich_log                      | 27.6 ms                                                    | 29.8 ms: 1.08x slower                                                  |
| async_tree_eager                 | 60.3 ms                                                    | 65.3 ms: 1.08x slower                                                  |
| sympy_sum                        | 69.2 ms                                                    | 75.0 ms: 1.08x slower                                                  |
| logging_simple                   | 3.04 us                                                    | 3.30 us: 1.09x slower                                                  |
| logging_format                   | 3.31 us                                                    | 3.60 us: 1.09x slower                                                  |
| logging_silent                   | 60.1 ns                                                    | 65.5 ns: 1.09x slower                                                  |
| scimark_fft                      | 181 ms                                                     | 199 ms: 1.10x slower                                                   |
| bench_thread_pool                | 447 us                                                     | 493 us: 1.10x slower                                                   |
| xml_etree_process                | 37.1 ms                                                    | 41.1 ms: 1.11x slower                                                  |
| spectral_norm                    | 66.4 ms                                                    | 74.5 ms: 1.12x slower                                                  |
| coroutines                       | 15.8 ms                                                    | 17.8 ms: 1.12x slower                                                  |
| sqlglot_optimize                 | 30.9 ms                                                    | 34.7 ms: 1.12x slower                                                  |
| scimark_sor                      | 94.9 ms                                                    | 107 ms: 1.13x slower                                                   |
| sqlglot_parse                    | 732 us                                                     | 826 us: 1.13x slower                                                   |
| sqlglot_transpile                | 891 us                                                     | 1.01 ms: 1.13x slower                                                  |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.14 ms: 1.13x slower                                                  |
| chaos                            | 34.0 ms                                                    | 38.6 ms: 1.13x slower                                                  |
| xml_etree_generate               | 52.7 ms                                                    | 60.2 ms: 1.14x slower                                                  |
| bench_mp_pool                    | 47.2 ms                                                    | 54.0 ms: 1.14x slower                                                  |
| deltablue                        | 2.14 ms                                                    | 2.46 ms: 1.15x slower                                                  |
| aiohttp                          | 997 us                                                     | 1.17 ms: 1.17x slower                                                  |
| python_startup                   | 15.2 ms                                                    | 17.8 ms: 1.17x slower                                                  |
| nbody                            | 59.6 ms                                                    | 70.3 ms: 1.18x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 61.6 ms: 1.18x slower                                                  |
| generators                       | 22.9 ms                                                    | 27.1 ms: 1.18x slower                                                  |
| hexiom                           | 4.06 ms                                                    | 4.82 ms: 1.19x slower                                                  |
| genshi_xml                       | 29.9 ms                                                    | 35.7 ms: 1.19x slower                                                  |
| 2to3                             | 161 ms                                                     | 192 ms: 1.20x slower                                                   |
| regex_compile                    | 68.5 ms                                                    | 82.0 ms: 1.20x slower                                                  |
| comprehensions                   | 10.2 us                                                    | 12.2 us: 1.20x slower                                                  |
| gunicorn                         | 1.04 ms                                                    | 1.25 ms: 1.21x slower                                                  |
| scimark_lu                       | 66.9 ms                                                    | 81.4 ms: 1.22x slower                                                  |
| raytrace                         | 147 ms                                                     | 179 ms: 1.22x slower                                                   |
| html5lib                         | 31.2 ms                                                    | 38.1 ms: 1.22x slower                                                  |
| async_generators                 | 281 ms                                                     | 344 ms: 1.23x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 407 ms: 1.23x slower                                                   |
| xml_etree_parse                  | 106 ms                                                     | 132 ms: 1.25x slower                                                   |
| tornado_http                     | 66.7 ms                                                    | 83.9 ms: 1.26x slower                                                  |
| python_startup_no_site           | 12.3 ms                                                    | 16.1 ms: 1.31x slower                                                  |
| pycparser                        | 632 ms                                                     | 840 ms: 1.33x slower                                                   |
| mypy2                            | 379 ms                                                     | 531 ms: 1.40x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 515 ms: 1.44x slower                                                   |
| xml_etree_iterparse              | 71.5 ms                                                    | 106 ms: 1.48x slower                                                   |
| docutils                         | 1.44 sec                                                   | 2.60 sec: 1.81x slower                                                 |
| float                            | 48.6 ms                                                    | 89.5 ms: 1.84x slower                                                  |
| dask                             | 221 ms                                                     | 456 ms: 2.06x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 331 ms: 2.64x slower                                                   |
| pylint                           | 170 ms                                                     | 588 ms: 3.46x slower                                                   |
| async_tree_eager_memoization     | 152 ms                                                     | 647 ms: 4.25x slower                                                   |
| async_tree_cpu_io_mixed          | 467 ms                                                     | 2.80 sec: 5.98x slower                                                 |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 2.96 sec: 6.56x slower                                                 |
| async_tree_none                  | 209 ms                                                     | 2.21 sec: 10.55x slower                                                |
| async_tree_memoization           | 260 ms                                                     | 2.82 sec: 10.88x slower                                                |
| async_tree_none_tg               | 198 ms                                                     | 2.44 sec: 12.35x slower                                                |
| async_tree_memoization_tg        | 240 ms                                                     | 2.96 sec: 12.37x slower                                                |
| async_tree_io                    | 563 ms                                                     | 8.92 sec: 15.83x slower                                                |
| async_tree_io_tg                 | 565 ms                                                     | 9.35 sec: 16.56x slower                                                |
| async_tree_eager_io              | 766 ms                                                     | 16.9 sec: 22.08x slower                                                |
| async_tree_eager_io_tg           | 768 ms                                                     | 18.0 sec: 23.40x slower                                                |
| Geometric mean                   | (ref)                                                      | 1.43x slower                                                           |

Benchmark hidden because not significant (4): unpickle, json, pickle_list, asyncio_tcp
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240320-3.13.0a5+-dcaf33a-JIT/bm-20240320-darwin-arm64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.34x