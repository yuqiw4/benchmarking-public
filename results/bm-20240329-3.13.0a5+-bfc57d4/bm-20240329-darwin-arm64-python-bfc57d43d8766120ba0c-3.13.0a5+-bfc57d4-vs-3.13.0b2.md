# Results vs. 3.13.0b2

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: darwin-arm64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 165 ms: 1.02x slower                                                   |
| chameleon      | 4.27 ms                                                    | 4.60 ms: 1.08x slower                                                  |
| docutils       | 1.44 sec                                                   | 1.48 sec: 1.03x slower                                                 |
| html5lib       | 31.2 ms                                                    | 34.0 ms: 1.09x slower                                                  |
| tornado_http   | 66.7 ms                                                    | 76.3 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                      | 1.07x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_io              | 766 ms                                                     | 733 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed          | 467 ms                                                     | 456 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 353 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.02x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 129 ms: 1.03x slower                                                   |
| async_tree_none                  | 209 ms                                                     | 218 ms: 1.04x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 64.2 ms: 1.06x slower                                                  |
| async_tree_eager_tg              | 41.4 ms                                                    | 45.1 ms: 1.09x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (8): async_tree_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| float          | 48.6 ms                                                    | 51.9 ms: 1.07x slower                                                  |
| nbody          | 59.6 ms                                                    | 66.1 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                      | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 17.3 ms                                                    | 17.0 ms: 1.02x faster                                                  |
| regex_compile  | 68.5 ms                                                    | 69.7 ms: 1.02x slower                                                  |
| regex_dna      | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| pickle_list          | 2.96 us                                                    | 3.00 us: 1.01x slower                                                  |
| tomli_loads          | 1.47 sec                                                   | 1.49 sec: 1.02x slower                                                 |
| unpickle             | 9.12 us                                                    | 9.27 us: 1.02x slower                                                  |
| xml_etree_iterparse  | 71.5 ms                                                    | 72.8 ms: 1.02x slower                                                  |
| json_loads           | 16.8 us                                                    | 17.1 us: 1.02x slower                                                  |
| xml_etree_process    | 37.1 ms                                                    | 37.8 ms: 1.02x slower                                                  |
| xml_etree_parse      | 106 ms                                                     | 109 ms: 1.03x slower                                                   |
| pickle_pure_python   | 179 us                                                     | 185 us: 1.04x slower                                                   |
| xml_etree_generate   | 52.7 ms                                                    | 55.2 ms: 1.05x slower                                                  |
| unpickle_list        | 2.88 us                                                    | 3.04 us: 1.05x slower                                                  |
| unpickle_pure_python | 141 us                                                     | 150 us: 1.07x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.02x slower                                                           |

Benchmark hidden because not significant (2): pickle, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                    | 11.9 ms: 1.27x faster                                                  |
| python_startup_no_site | 12.3 ms                                                    | 10.2 ms: 1.20x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.24x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 6.95 ms: 1.00x faster                                                  |
| genshi_text     | 13.9 ms                                                    | 14.6 ms: 1.05x slower                                                  |
| genshi_xml      | 29.9 ms                                                    | 31.5 ms: 1.05x slower                                                  |
| django_template | 19.4 ms                                                    | 20.7 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup                   | 15.2 ms                                                    | 11.9 ms: 1.27x faster                                                  |
| typing_runtime_protocols         | 87.6 us                                                    | 70.8 us: 1.24x faster                                                  |
| python_startup_no_site           | 12.3 ms                                                    | 10.2 ms: 1.20x faster                                                  |
| pylint                           | 170 ms                                                     | 149 ms: 1.14x faster                                                   |
| bench_mp_pool                    | 47.2 ms                                                    | 42.9 ms: 1.10x faster                                                  |
| create_gc_cycles                 | 897 us                                                     | 835 us: 1.07x faster                                                   |
| crypto_pyaes                     | 49.5 ms                                                    | 47.2 ms: 1.05x faster                                                  |
| async_tree_eager_io              | 766 ms                                                     | 733 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed          | 467 ms                                                     | 456 ms: 1.02x faster                                                   |
| richards                         | 31.8 ms                                                    | 31.3 ms: 1.02x faster                                                  |
| regex_v8                         | 17.3 ms                                                    | 17.0 ms: 1.02x faster                                                  |
| telco                            | 4.60 ms                                                    | 4.54 ms: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 353 ms: 1.01x faster                                                   |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| richards_super                   | 35.2 ms                                                    | 34.9 ms: 1.01x faster                                                  |
| gc_traversal                     | 2.45 ms                                                    | 2.43 ms: 1.01x faster                                                  |
| mako                             | 6.99 ms                                                    | 6.95 ms: 1.00x faster                                                  |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                   |
| pidigits                         | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| sympy_str                        | 131 ms                                                     | 132 ms: 1.01x slower                                                   |
| comprehensions                   | 10.2 us                                                    | 10.2 us: 1.01x slower                                                  |
| sympy_sum                        | 69.2 ms                                                    | 70.0 ms: 1.01x slower                                                  |
| sqlite_synth                     | 1.55 us                                                    | 1.57 us: 1.01x slower                                                  |
| meteor_contest                   | 70.3 ms                                                    | 71.3 ms: 1.01x slower                                                  |
| pickle_list                      | 2.96 us                                                    | 3.00 us: 1.01x slower                                                  |
| thrift                           | 435 us                                                     | 442 us: 1.01x slower                                                   |
| json                             | 2.93 ms                                                    | 2.97 ms: 1.01x slower                                                  |
| tomli_loads                      | 1.47 sec                                                   | 1.49 sec: 1.02x slower                                                 |
| unpickle                         | 9.12 us                                                    | 9.27 us: 1.02x slower                                                  |
| regex_compile                    | 68.5 ms                                                    | 69.7 ms: 1.02x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.02x slower                                                   |
| xml_etree_iterparse              | 71.5 ms                                                    | 72.8 ms: 1.02x slower                                                  |
| json_loads                       | 16.8 us                                                    | 17.1 us: 1.02x slower                                                  |
| regex_dna                        | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| async_generators                 | 281 ms                                                     | 286 ms: 1.02x slower                                                   |
| xml_etree_process                | 37.1 ms                                                    | 37.8 ms: 1.02x slower                                                  |
| pyflate                          | 321 ms                                                     | 329 ms: 1.02x slower                                                   |
| 2to3                             | 161 ms                                                     | 165 ms: 1.02x slower                                                   |
| xml_etree_parse                  | 106 ms                                                     | 109 ms: 1.03x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 129 ms: 1.03x slower                                                   |
| scimark_lu                       | 66.9 ms                                                    | 68.9 ms: 1.03x slower                                                  |
| sqlglot_transpile                | 891 us                                                     | 918 us: 1.03x slower                                                   |
| docutils                         | 1.44 sec                                                   | 1.48 sec: 1.03x slower                                                 |
| sqlglot_parse                    | 732 us                                                     | 756 us: 1.03x slower                                                   |
| pickle_pure_python               | 179 us                                                     | 185 us: 1.04x slower                                                   |
| coverage                         | 45.0 ms                                                    | 46.8 ms: 1.04x slower                                                  |
| sqlglot_optimize                 | 30.9 ms                                                    | 32.1 ms: 1.04x slower                                                  |
| sqlglot_normalize                | 166 ms                                                     | 172 ms: 1.04x slower                                                   |
| pycparser                        | 632 ms                                                     | 660 ms: 1.04x slower                                                   |
| async_tree_none                  | 209 ms                                                     | 218 ms: 1.04x slower                                                   |
| pprint_pformat                   | 947 ms                                                     | 989 ms: 1.05x slower                                                   |
| pprint_safe_repr                 | 465 ms                                                     | 486 ms: 1.05x slower                                                   |
| dulwich_log                      | 27.6 ms                                                    | 28.9 ms: 1.05x slower                                                  |
| deepcopy_reduce                  | 1.82 us                                                    | 1.91 us: 1.05x slower                                                  |
| xml_etree_generate               | 52.7 ms                                                    | 55.2 ms: 1.05x slower                                                  |
| genshi_text                      | 13.9 ms                                                    | 14.6 ms: 1.05x slower                                                  |
| scimark_monte_carlo              | 42.5 ms                                                    | 44.6 ms: 1.05x slower                                                  |
| hexiom                           | 4.06 ms                                                    | 4.27 ms: 1.05x slower                                                  |
| genshi_xml                       | 29.9 ms                                                    | 31.5 ms: 1.05x slower                                                  |
| unpickle_list                    | 2.88 us                                                    | 3.04 us: 1.05x slower                                                  |
| deepcopy                         | 204 us                                                     | 215 us: 1.06x slower                                                   |
| pathlib                          | 23.3 ms                                                    | 24.6 ms: 1.06x slower                                                  |
| deepcopy_memo                    | 22.6 us                                                    | 23.9 us: 1.06x slower                                                  |
| fannkuch                         | 248 ms                                                     | 263 ms: 1.06x slower                                                   |
| gunicorn                         | 1.04 ms                                                    | 1.10 ms: 1.06x slower                                                  |
| scimark_sor                      | 94.9 ms                                                    | 101 ms: 1.06x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 64.2 ms: 1.06x slower                                                  |
| unpickle_pure_python             | 141 us                                                     | 150 us: 1.07x slower                                                   |
| bench_thread_pool                | 447 us                                                     | 476 us: 1.07x slower                                                   |
| django_template                  | 19.4 ms                                                    | 20.7 ms: 1.07x slower                                                  |
| raytrace                         | 147 ms                                                     | 157 ms: 1.07x slower                                                   |
| float                            | 48.6 ms                                                    | 51.9 ms: 1.07x slower                                                  |
| aiohttp                          | 997 us                                                     | 1.07 ms: 1.07x slower                                                  |
| chaos                            | 34.0 ms                                                    | 36.5 ms: 1.07x slower                                                  |
| spectral_norm                    | 66.4 ms                                                    | 71.3 ms: 1.07x slower                                                  |
| coroutines                       | 15.8 ms                                                    | 17.0 ms: 1.07x slower                                                  |
| deltablue                        | 2.14 ms                                                    | 2.30 ms: 1.07x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 56.2 ms: 1.08x slower                                                  |
| scimark_fft                      | 181 ms                                                     | 195 ms: 1.08x slower                                                   |
| chameleon                        | 4.27 ms                                                    | 4.60 ms: 1.08x slower                                                  |
| async_tree_eager_tg              | 41.4 ms                                                    | 45.1 ms: 1.09x slower                                                  |
| html5lib                         | 31.2 ms                                                    | 34.0 ms: 1.09x slower                                                  |
| logging_silent                   | 60.1 ns                                                    | 65.9 ns: 1.10x slower                                                  |
| logging_format                   | 3.31 us                                                    | 3.62 us: 1.10x slower                                                  |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.05 ms: 1.10x slower                                                  |
| logging_simple                   | 3.04 us                                                    | 3.34 us: 1.10x slower                                                  |
| nbody                            | 59.6 ms                                                    | 66.1 ms: 1.11x slower                                                  |
| tornado_http                     | 66.7 ms                                                    | 76.3 ms: 1.14x slower                                                  |
| generators                       | 22.9 ms                                                    | 27.7 ms: 1.21x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.02x slower                                                           |

Benchmark hidden because not significant (19): dask, async_tree_io, async_tree_eager_io_tg, mdp, pickle, go, sympy_integrate, json_dumps, regex_effbot, async_tree_eager_memoization, asyncio_tcp_ssl, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_none_tg, mypy2, async_tree_io_tg, async_tree_memoization_tg, asyncio_tcp, sympy_expand
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-darwin-arm64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.96x