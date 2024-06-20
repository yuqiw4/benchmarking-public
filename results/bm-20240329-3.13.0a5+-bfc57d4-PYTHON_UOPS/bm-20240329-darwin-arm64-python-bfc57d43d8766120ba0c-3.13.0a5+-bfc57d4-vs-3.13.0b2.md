# Results vs. 3.13.0b2

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: darwin-arm64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.13x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 178 ms: 1.11x slower                                                   |
| chameleon      | 4.27 ms                                                    | 4.83 ms: 1.13x slower                                                  |
| docutils       | 1.44 sec                                                   | 1.62 sec: 1.12x slower                                                 |
| html5lib       | 31.2 ms                                                    | 35.0 ms: 1.12x slower                                                  |
| tornado_http   | 66.7 ms                                                    | 80.3 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                      | 1.14x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 338 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 464 ms: 1.03x slower                                                   |
| async_tree_io                    | 563 ms                                                     | 584 ms: 1.04x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 132 ms: 1.05x slower                                                   |
| async_tree_none_tg               | 198 ms                                                     | 209 ms: 1.06x slower                                                   |
| async_tree_memoization           | 260 ms                                                     | 276 ms: 1.07x slower                                                   |
| async_tree_memoization_tg        | 240 ms                                                     | 270 ms: 1.13x slower                                                   |
| async_tree_none                  | 209 ms                                                     | 236 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 47.3 ms: 1.14x slower                                                  |
| async_tree_eager                 | 60.3 ms                                                    | 69.9 ms: 1.16x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.05x slower                                                           |

Benchmark hidden because not significant (6): async_tree_eager_io, async_tree_eager_cpu_io_mixed, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_eager_io_tg, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 283 ms: 1.01x slower                                                   |
| float          | 48.6 ms                                                    | 69.4 ms: 1.43x slower                                                  |
| nbody          | 59.6 ms                                                    | 86.7 ms: 1.45x slower                                                  |
| Geometric mean | (ref)                                                      | 1.28x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.58 ms                                                    | 2.56 ms: 1.01x faster                                                  |
| regex_v8       | 17.3 ms                                                    | 17.2 ms: 1.00x faster                                                  |
| regex_dna      | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| regex_compile  | 68.5 ms                                                    | 92.7 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                      | 1.08x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| pickle               | 7.48 us                                                    | 7.52 us: 1.01x slower                                                  |
| json_dumps           | 6.23 ms                                                    | 6.28 ms: 1.01x slower                                                  |
| xml_etree_parse      | 106 ms                                                     | 107 ms: 1.01x slower                                                   |
| json_loads           | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| pickle_list          | 2.96 us                                                    | 3.01 us: 1.02x slower                                                  |
| pickle_pure_python   | 179 us                                                     | 189 us: 1.06x slower                                                   |
| xml_etree_process    | 37.1 ms                                                    | 39.2 ms: 1.06x slower                                                  |
| unpickle_list        | 2.88 us                                                    | 3.05 us: 1.06x slower                                                  |
| xml_etree_iterparse  | 71.5 ms                                                    | 79.5 ms: 1.11x slower                                                  |
| xml_etree_generate   | 52.7 ms                                                    | 58.9 ms: 1.12x slower                                                  |
| tomli_loads          | 1.47 sec                                                   | 1.69 sec: 1.15x slower                                                 |
| unpickle_pure_python | 141 us                                                     | 188 us: 1.33x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.06x slower                                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                    | 12.0 ms: 1.27x faster                                                  |
| python_startup_no_site | 12.3 ms                                                    | 10.3 ms: 1.20x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.23x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 29.9 ms                                                    | 33.1 ms: 1.11x slower                                                  |
| genshi_text     | 13.9 ms                                                    | 15.4 ms: 1.11x slower                                                  |
| django_template | 19.4 ms                                                    | 22.6 ms: 1.17x slower                                                  |
| mako            | 6.99 ms                                                    | 9.32 ms: 1.33x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.18x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup                   | 15.2 ms                                                    | 12.0 ms: 1.27x faster                                                  |
| typing_runtime_protocols         | 87.6 us                                                    | 72.6 us: 1.21x faster                                                  |
| python_startup_no_site           | 12.3 ms                                                    | 10.3 ms: 1.20x faster                                                  |
| bench_mp_pool                    | 47.2 ms                                                    | 43.8 ms: 1.08x faster                                                  |
| pylint                           | 170 ms                                                     | 159 ms: 1.07x faster                                                   |
| create_gc_cycles                 | 897 us                                                     | 845 us: 1.06x faster                                                   |
| regex_effbot                     | 2.58 ms                                                    | 2.56 ms: 1.01x faster                                                  |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| regex_v8                         | 17.3 ms                                                    | 17.2 ms: 1.00x faster                                                  |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                   |
| gc_traversal                     | 2.45 ms                                                    | 2.45 ms: 1.00x faster                                                  |
| pidigits                         | 282 ms                                                     | 283 ms: 1.01x slower                                                   |
| pickle                           | 7.48 us                                                    | 7.52 us: 1.01x slower                                                  |
| json_dumps                       | 6.23 ms                                                    | 6.28 ms: 1.01x slower                                                  |
| xml_etree_parse                  | 106 ms                                                     | 107 ms: 1.01x slower                                                   |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| json                             | 2.93 ms                                                    | 2.98 ms: 1.02x slower                                                  |
| pickle_list                      | 2.96 us                                                    | 3.01 us: 1.02x slower                                                  |
| regex_dna                        | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 338 ms: 1.02x slower                                                   |
| thrift                           | 435 us                                                     | 447 us: 1.03x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 464 ms: 1.03x slower                                                   |
| async_tree_io                    | 563 ms                                                     | 584 ms: 1.04x slower                                                   |
| coverage                         | 45.0 ms                                                    | 46.7 ms: 1.04x slower                                                  |
| telco                            | 4.60 ms                                                    | 4.80 ms: 1.04x slower                                                  |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 132 ms: 1.05x slower                                                   |
| deepcopy_reduce                  | 1.82 us                                                    | 1.92 us: 1.05x slower                                                  |
| pickle_pure_python               | 179 us                                                     | 189 us: 1.06x slower                                                   |
| async_tree_none_tg               | 198 ms                                                     | 209 ms: 1.06x slower                                                   |
| xml_etree_process                | 37.1 ms                                                    | 39.2 ms: 1.06x slower                                                  |
| unpickle_list                    | 2.88 us                                                    | 3.05 us: 1.06x slower                                                  |
| async_tree_memoization           | 260 ms                                                     | 276 ms: 1.07x slower                                                   |
| sqlite_synth                     | 1.55 us                                                    | 1.65 us: 1.07x slower                                                  |
| mdp                              | 1.53 sec                                                   | 1.64 sec: 1.07x slower                                                 |
| coroutines                       | 15.8 ms                                                    | 17.0 ms: 1.07x slower                                                  |
| pathlib                          | 23.3 ms                                                    | 25.1 ms: 1.08x slower                                                  |
| aiohttp                          | 997 us                                                     | 1.08 ms: 1.08x slower                                                  |
| async_generators                 | 281 ms                                                     | 303 ms: 1.08x slower                                                   |
| asyncio_tcp                      | 402 ms                                                     | 436 ms: 1.08x slower                                                   |
| deepcopy                         | 204 us                                                     | 222 us: 1.09x slower                                                   |
| sympy_expand                     | 226 ms                                                     | 247 ms: 1.09x slower                                                   |
| mypy2                            | 379 ms                                                     | 417 ms: 1.10x slower                                                   |
| dulwich_log                      | 27.6 ms                                                    | 30.4 ms: 1.10x slower                                                  |
| 2to3                             | 161 ms                                                     | 178 ms: 1.11x slower                                                   |
| genshi_xml                       | 29.9 ms                                                    | 33.1 ms: 1.11x slower                                                  |
| genshi_text                      | 13.9 ms                                                    | 15.4 ms: 1.11x slower                                                  |
| xml_etree_iterparse              | 71.5 ms                                                    | 79.5 ms: 1.11x slower                                                  |
| logging_format                   | 3.31 us                                                    | 3.68 us: 1.11x slower                                                  |
| logging_simple                   | 3.04 us                                                    | 3.39 us: 1.12x slower                                                  |
| pycparser                        | 632 ms                                                     | 705 ms: 1.12x slower                                                   |
| xml_etree_generate               | 52.7 ms                                                    | 58.9 ms: 1.12x slower                                                  |
| sqlglot_normalize                | 166 ms                                                     | 186 ms: 1.12x slower                                                   |
| html5lib                         | 31.2 ms                                                    | 35.0 ms: 1.12x slower                                                  |
| docutils                         | 1.44 sec                                                   | 1.62 sec: 1.12x slower                                                 |
| async_tree_memoization_tg        | 240 ms                                                     | 270 ms: 1.13x slower                                                   |
| async_tree_none                  | 209 ms                                                     | 236 ms: 1.13x slower                                                   |
| logging_silent                   | 60.1 ns                                                    | 67.9 ns: 1.13x slower                                                  |
| chameleon                        | 4.27 ms                                                    | 4.83 ms: 1.13x slower                                                  |
| gunicorn                         | 1.04 ms                                                    | 1.18 ms: 1.13x slower                                                  |
| sqlglot_transpile                | 891 us                                                     | 1.01 ms: 1.14x slower                                                  |
| async_tree_eager_tg              | 41.4 ms                                                    | 47.3 ms: 1.14x slower                                                  |
| crypto_pyaes                     | 49.5 ms                                                    | 56.7 ms: 1.15x slower                                                  |
| tomli_loads                      | 1.47 sec                                                   | 1.69 sec: 1.15x slower                                                 |
| sqlglot_parse                    | 732 us                                                     | 843 us: 1.15x slower                                                   |
| meteor_contest                   | 70.3 ms                                                    | 81.1 ms: 1.15x slower                                                  |
| sqlglot_optimize                 | 30.9 ms                                                    | 35.7 ms: 1.16x slower                                                  |
| bench_thread_pool                | 447 us                                                     | 517 us: 1.16x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 69.9 ms: 1.16x slower                                                  |
| sympy_integrate                  | 10.3 ms                                                    | 12.0 ms: 1.16x slower                                                  |
| sympy_str                        | 131 ms                                                     | 153 ms: 1.16x slower                                                   |
| django_template                  | 19.4 ms                                                    | 22.6 ms: 1.17x slower                                                  |
| go                               | 101 ms                                                     | 118 ms: 1.17x slower                                                   |
| richards_super                   | 35.2 ms                                                    | 41.8 ms: 1.19x slower                                                  |
| sympy_sum                        | 69.2 ms                                                    | 82.3 ms: 1.19x slower                                                  |
| richards                         | 31.8 ms                                                    | 38.1 ms: 1.20x slower                                                  |
| tornado_http                     | 66.7 ms                                                    | 80.3 ms: 1.20x slower                                                  |
| generators                       | 22.9 ms                                                    | 28.0 ms: 1.22x slower                                                  |
| deltablue                        | 2.14 ms                                                    | 2.63 ms: 1.23x slower                                                  |
| scimark_sor                      | 94.9 ms                                                    | 117 ms: 1.23x slower                                                   |
| deepcopy_memo                    | 22.6 us                                                    | 28.0 us: 1.24x slower                                                  |
| pprint_safe_repr                 | 465 ms                                                     | 580 ms: 1.25x slower                                                   |
| pprint_pformat                   | 947 ms                                                     | 1.18 sec: 1.25x slower                                                 |
| unpickle_pure_python             | 141 us                                                     | 188 us: 1.33x slower                                                   |
| mako                             | 6.99 ms                                                    | 9.32 ms: 1.33x slower                                                  |
| pyflate                          | 321 ms                                                     | 434 ms: 1.35x slower                                                   |
| regex_compile                    | 68.5 ms                                                    | 92.7 ms: 1.35x slower                                                  |
| scimark_fft                      | 181 ms                                                     | 249 ms: 1.38x slower                                                   |
| fannkuch                         | 248 ms                                                     | 347 ms: 1.40x slower                                                   |
| chaos                            | 34.0 ms                                                    | 48.0 ms: 1.41x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 74.1 ms: 1.42x slower                                                  |
| float                            | 48.6 ms                                                    | 69.4 ms: 1.43x slower                                                  |
| nbody                            | 59.6 ms                                                    | 86.7 ms: 1.45x slower                                                  |
| raytrace                         | 147 ms                                                     | 215 ms: 1.46x slower                                                   |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 4.19 ms: 1.51x slower                                                  |
| spectral_norm                    | 66.4 ms                                                    | 102 ms: 1.54x slower                                                   |
| scimark_monte_carlo              | 42.5 ms                                                    | 65.4 ms: 1.54x slower                                                  |
| scimark_lu                       | 66.9 ms                                                    | 104 ms: 1.55x slower                                                   |
| hexiom                           | 4.06 ms                                                    | 6.31 ms: 1.56x slower                                                  |
| comprehensions                   | 10.2 us                                                    | 17.4 us: 1.71x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.13x slower                                                           |

Benchmark hidden because not significant (9): async_tree_eager_io, unpickle, async_tree_eager_cpu_io_mixed, dask, async_tree_cpu_io_mixed, async_tree_io_tg, asyncio_tcp_ssl, async_tree_eager_io_tg, async_tree_eager_memoization
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-bfc57d4-PYTHON_UOPS/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 0.97x