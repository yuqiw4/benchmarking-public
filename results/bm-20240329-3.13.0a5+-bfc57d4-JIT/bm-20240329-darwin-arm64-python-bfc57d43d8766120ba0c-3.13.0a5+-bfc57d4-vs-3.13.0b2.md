# Results vs. 3.13.0b2

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: darwin-arm64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 173 ms: 1.08x slower                                                   |
| chameleon      | 4.27 ms                                                    | 4.46 ms: 1.05x slower                                                  |
| docutils       | 1.44 sec                                                   | 1.55 sec: 1.08x slower                                                 |
| html5lib       | 31.2 ms                                                    | 33.6 ms: 1.08x slower                                                  |
| tornado_http   | 66.7 ms                                                    | 79.6 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                      | 1.09x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_io              | 766 ms                                                     | 733 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 355 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 335 ms: 1.01x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 129 ms: 1.03x slower                                                   |
| async_tree_memoization_tg        | 240 ms                                                     | 249 ms: 1.04x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 44.7 ms: 1.08x slower                                                  |
| async_tree_none                  | 209 ms                                                     | 226 ms: 1.08x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 65.6 ms: 1.09x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.02x slower                                                           |

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_eager_io_tg, async_tree_io, async_tree_eager_memoization, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| float          | 48.6 ms                                                    | 49.2 ms: 1.01x slower                                                  |
| nbody          | 59.6 ms                                                    | 70.3 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                      | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 17.3 ms                                                    | 17.1 ms: 1.01x faster                                                  |
| regex_effbot   | 2.58 ms                                                    | 2.62 ms: 1.01x slower                                                  |
| regex_dna      | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| regex_compile  | 68.5 ms                                                    | 81.0 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                      | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 1.47 sec                                                   | 1.30 sec: 1.13x faster                                                 |
| pickle_dict          | 18.3 us                                                    | 18.0 us: 1.01x faster                                                  |
| xml_etree_process    | 37.1 ms                                                    | 36.8 ms: 1.01x faster                                                  |
| pickle               | 7.48 us                                                    | 7.44 us: 1.01x faster                                                  |
| json_loads           | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 71.5 ms                                                    | 72.3 ms: 1.01x slower                                                  |
| unpickle_pure_python | 141 us                                                     | 143 us: 1.02x slower                                                   |
| json_dumps           | 6.23 ms                                                    | 6.37 ms: 1.02x slower                                                  |
| pickle_pure_python   | 179 us                                                     | 183 us: 1.02x slower                                                   |
| xml_etree_generate   | 52.7 ms                                                    | 54.4 ms: 1.03x slower                                                  |
| unpickle_list        | 2.88 us                                                    | 3.05 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                           |

Benchmark hidden because not significant (3): pickle_list, unpickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                    | 13.4 ms: 1.13x faster                                                  |
| python_startup_no_site | 12.3 ms                                                    | 11.6 ms: 1.06x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.10x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 6.95 ms: 1.00x faster                                                  |
| genshi_xml      | 29.9 ms                                                    | 31.4 ms: 1.05x slower                                                  |
| django_template | 19.4 ms                                                    | 20.7 ms: 1.07x slower                                                  |
| genshi_text     | 13.9 ms                                                    | 14.9 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.05x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols         | 87.6 us                                                    | 69.6 us: 1.26x faster                                                  |
| python_startup                   | 15.2 ms                                                    | 13.4 ms: 1.13x faster                                                  |
| tomli_loads                      | 1.47 sec                                                   | 1.30 sec: 1.13x faster                                                 |
| pylint                           | 170 ms                                                     | 156 ms: 1.09x faster                                                   |
| python_startup_no_site           | 12.3 ms                                                    | 11.6 ms: 1.06x faster                                                  |
| create_gc_cycles                 | 897 us                                                     | 849 us: 1.06x faster                                                   |
| crypto_pyaes                     | 49.5 ms                                                    | 47.0 ms: 1.05x faster                                                  |
| async_tree_eager_io              | 766 ms                                                     | 733 ms: 1.05x faster                                                   |
| telco                            | 4.60 ms                                                    | 4.51 ms: 1.02x faster                                                  |
| bench_mp_pool                    | 47.2 ms                                                    | 46.4 ms: 1.02x faster                                                  |
| pickle_dict                      | 18.3 us                                                    | 18.0 us: 1.01x faster                                                  |
| richards                         | 31.8 ms                                                    | 31.5 ms: 1.01x faster                                                  |
| regex_v8                         | 17.3 ms                                                    | 17.1 ms: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 355 ms: 1.01x faster                                                   |
| richards_super                   | 35.2 ms                                                    | 34.9 ms: 1.01x faster                                                  |
| xml_etree_process                | 37.1 ms                                                    | 36.8 ms: 1.01x faster                                                  |
| pickle                           | 7.48 us                                                    | 7.44 us: 1.01x faster                                                  |
| mako                             | 6.99 ms                                                    | 6.95 ms: 1.00x faster                                                  |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                   |
| pidigits                         | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| thrift                           | 435 us                                                     | 437 us: 1.00x slower                                                   |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| xml_etree_iterparse              | 71.5 ms                                                    | 72.3 ms: 1.01x slower                                                  |
| float                            | 48.6 ms                                                    | 49.2 ms: 1.01x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 335 ms: 1.01x slower                                                   |
| regex_effbot                     | 2.58 ms                                                    | 2.62 ms: 1.01x slower                                                  |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.31 sec: 1.02x slower                                                 |
| unpickle_pure_python             | 141 us                                                     | 143 us: 1.02x slower                                                   |
| json                             | 2.93 ms                                                    | 2.98 ms: 1.02x slower                                                  |
| regex_dna                        | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| json_dumps                       | 6.23 ms                                                    | 6.37 ms: 1.02x slower                                                  |
| pickle_pure_python               | 179 us                                                     | 183 us: 1.02x slower                                                   |
| mdp                              | 1.53 sec                                                   | 1.57 sec: 1.02x slower                                                 |
| sqlite_synth                     | 1.55 us                                                    | 1.59 us: 1.03x slower                                                  |
| deepcopy_reduce                  | 1.82 us                                                    | 1.87 us: 1.03x slower                                                  |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 129 ms: 1.03x slower                                                   |
| xml_etree_generate               | 52.7 ms                                                    | 54.4 ms: 1.03x slower                                                  |
| pyflate                          | 321 ms                                                     | 332 ms: 1.03x slower                                                   |
| coverage                         | 45.0 ms                                                    | 46.7 ms: 1.04x slower                                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 249 ms: 1.04x slower                                                   |
| go                               | 101 ms                                                     | 105 ms: 1.04x slower                                                   |
| deepcopy                         | 204 us                                                     | 212 us: 1.04x slower                                                   |
| scimark_monte_carlo              | 42.5 ms                                                    | 44.2 ms: 1.04x slower                                                  |
| sqlglot_parse                    | 732 us                                                     | 765 us: 1.05x slower                                                   |
| chameleon                        | 4.27 ms                                                    | 4.46 ms: 1.05x slower                                                  |
| sympy_expand                     | 226 ms                                                     | 236 ms: 1.05x slower                                                   |
| genshi_xml                       | 29.9 ms                                                    | 31.4 ms: 1.05x slower                                                  |
| pprint_safe_repr                 | 465 ms                                                     | 487 ms: 1.05x slower                                                   |
| fannkuch                         | 248 ms                                                     | 261 ms: 1.05x slower                                                   |
| sqlglot_transpile                | 891 us                                                     | 935 us: 1.05x slower                                                   |
| coroutines                       | 15.8 ms                                                    | 16.7 ms: 1.05x slower                                                  |
| meteor_contest                   | 70.3 ms                                                    | 74.1 ms: 1.05x slower                                                  |
| sqlglot_normalize                | 166 ms                                                     | 175 ms: 1.06x slower                                                   |
| gc_traversal                     | 2.45 ms                                                    | 2.59 ms: 1.06x slower                                                  |
| unpickle_list                    | 2.88 us                                                    | 3.05 us: 1.06x slower                                                  |
| pprint_pformat                   | 947 ms                                                     | 1.00 sec: 1.06x slower                                                 |
| pycparser                        | 632 ms                                                     | 671 ms: 1.06x slower                                                   |
| sympy_str                        | 131 ms                                                     | 140 ms: 1.07x slower                                                   |
| pathlib                          | 23.3 ms                                                    | 24.9 ms: 1.07x slower                                                  |
| django_template                  | 19.4 ms                                                    | 20.7 ms: 1.07x slower                                                  |
| async_generators                 | 281 ms                                                     | 300 ms: 1.07x slower                                                   |
| genshi_text                      | 13.9 ms                                                    | 14.9 ms: 1.07x slower                                                  |
| deepcopy_memo                    | 22.6 us                                                    | 24.3 us: 1.07x slower                                                  |
| 2to3                             | 161 ms                                                     | 173 ms: 1.08x slower                                                   |
| html5lib                         | 31.2 ms                                                    | 33.6 ms: 1.08x slower                                                  |
| async_tree_eager_tg              | 41.4 ms                                                    | 44.7 ms: 1.08x slower                                                  |
| logging_format                   | 3.31 us                                                    | 3.58 us: 1.08x slower                                                  |
| async_tree_none                  | 209 ms                                                     | 226 ms: 1.08x slower                                                   |
| docutils                         | 1.44 sec                                                   | 1.55 sec: 1.08x slower                                                 |
| logging_simple                   | 3.04 us                                                    | 3.29 us: 1.08x slower                                                  |
| sqlglot_optimize                 | 30.9 ms                                                    | 33.6 ms: 1.09x slower                                                  |
| mypy2                            | 379 ms                                                     | 413 ms: 1.09x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 65.6 ms: 1.09x slower                                                  |
| dulwich_log                      | 27.6 ms                                                    | 30.0 ms: 1.09x slower                                                  |
| logging_silent                   | 60.1 ns                                                    | 65.7 ns: 1.09x slower                                                  |
| sympy_integrate                  | 10.3 ms                                                    | 11.3 ms: 1.09x slower                                                  |
| aiohttp                          | 997 us                                                     | 1.09 ms: 1.10x slower                                                  |
| sympy_sum                        | 69.2 ms                                                    | 75.9 ms: 1.10x slower                                                  |
| deltablue                        | 2.14 ms                                                    | 2.36 ms: 1.10x slower                                                  |
| bench_thread_pool                | 447 us                                                     | 494 us: 1.10x slower                                                   |
| scimark_fft                      | 181 ms                                                     | 200 ms: 1.10x slower                                                   |
| spectral_norm                    | 66.4 ms                                                    | 73.7 ms: 1.11x slower                                                  |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.13 ms: 1.13x slower                                                  |
| chaos                            | 34.0 ms                                                    | 38.5 ms: 1.13x slower                                                  |
| scimark_sor                      | 94.9 ms                                                    | 107 ms: 1.13x slower                                                   |
| generators                       | 22.9 ms                                                    | 26.4 ms: 1.15x slower                                                  |
| gunicorn                         | 1.04 ms                                                    | 1.20 ms: 1.15x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 60.5 ms: 1.16x slower                                                  |
| nbody                            | 59.6 ms                                                    | 70.3 ms: 1.18x slower                                                  |
| regex_compile                    | 68.5 ms                                                    | 81.0 ms: 1.18x slower                                                  |
| comprehensions                   | 10.2 us                                                    | 12.0 us: 1.18x slower                                                  |
| tornado_http                     | 66.7 ms                                                    | 79.6 ms: 1.19x slower                                                  |
| scimark_lu                       | 66.9 ms                                                    | 81.6 ms: 1.22x slower                                                  |
| raytrace                         | 147 ms                                                     | 180 ms: 1.22x slower                                                   |
| hexiom                           | 4.06 ms                                                    | 4.96 ms: 1.22x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.04x slower                                                           |

Benchmark hidden because not significant (13): async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_eager_io_tg, dask, pickle_list, unpickle, async_tree_io, xml_etree_parse, asyncio_tcp, async_tree_eager_memoization, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.18x