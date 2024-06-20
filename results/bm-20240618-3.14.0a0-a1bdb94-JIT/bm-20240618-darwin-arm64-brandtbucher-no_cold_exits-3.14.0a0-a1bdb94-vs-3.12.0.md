# Results vs. 3.12.0

- fork: brandtbucher
- ref: no_cold_exits
- machine: darwin-arm64
- commit hash: a1bdb94
- commit date: 2024-06-18
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (3): 2to3, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240618-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-a1bdb94 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 258 ms                                                 | 196 ms: 1.31x faster                                                 |
| async_tree_memoization_tg  | 323 ms                                                 | 253 ms: 1.28x faster                                                 |
| async_tree_none            | 266 ms                                                 | 217 ms: 1.23x faster                                                 |
| async_tree_io_tg           | 669 ms                                                 | 555 ms: 1.21x faster                                                 |
| async_tree_memoization     | 312 ms                                                 | 268 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 457 ms: 1.17x faster                                                 |
| async_tree_io              | 668 ms                                                 | 580 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 476 ms: 1.10x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.20x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240618-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-a1bdb94 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 55.8 ms                                                | 46.4 ms: 1.20x faster                                                |
| nbody          | 68.8 ms                                                | 63.6 ms: 1.08x faster                                                |
| pidigits       | 282 ms                                                 | 286 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240618-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-a1bdb94 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 77.9 ms                                                | 72.1 ms: 1.08x faster                                                |
| regex_dna      | 154 ms                                                 | 149 ms: 1.03x faster                                                 |
| regex_effbot   | 2.64 ms                                                | 2.56 ms: 1.03x faster                                                |
| regex_v8       | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240618-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-a1bdb94 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 151 us                                                 | 132 us: 1.14x faster                                                 |
| pickle_pure_python   | 200 us                                                 | 176 us: 1.14x faster                                                 |
| tomli_loads          | 1.39 sec                                               | 1.27 sec: 1.10x faster                                               |
| xml_etree_process    | 39.7 ms                                                | 36.1 ms: 1.10x faster                                                |
| xml_etree_generate   | 55.8 ms                                                | 52.2 ms: 1.07x faster                                                |
| xml_etree_iterparse  | 74.0 ms                                                | 71.3 ms: 1.04x faster                                                |
| unpickle_list        | 3.02 us                                                | 2.93 us: 1.03x faster                                                |
| json_loads           | 17.2 us                                                | 17.0 us: 1.01x faster                                                |
| json_dumps           | 6.22 ms                                                | 6.26 ms: 1.01x slower                                                |
| unpickle             | 9.12 us                                                | 9.32 us: 1.02x slower                                                |
| pickle_dict          | 18.1 us                                                | 18.6 us: 1.03x slower                                                |
| pickle               | 7.23 us                                                | 7.49 us: 1.04x slower                                                |
| pickle_list          | 2.89 us                                                | 3.02 us: 1.05x slower                                                |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240618-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-a1bdb94 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 11.4 ms                                                | 14.9 ms: 1.31x slower                                                |
| python_startup_no_site | 9.37 ms                                                | 12.3 ms: 1.31x slower                                                |
| Geometric mean         | (ref)                                                  | 1.31x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240618-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-a1bdb94 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 7.71 ms                                                | 6.46 ms: 1.19x faster                                                |
| django_template | 22.3 ms                                                | 21.9 ms: 1.02x faster                                                |
| Geometric mean  | (ref)                                                  | 1.10x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240618-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-a1bdb94 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| deepcopy_memo              | 27.7 us                                                | 16.8 us: 1.64x faster                                                |
| deepcopy                   | 235 us                                                 | 155 us: 1.52x faster                                                 |
| generators                 | 31.1 ms                                                | 23.2 ms: 1.34x faster                                                |
| deepcopy_reduce            | 2.07 us                                                | 1.55 us: 1.34x faster                                                |
| async_tree_none_tg         | 258 ms                                                 | 196 ms: 1.31x faster                                                 |
| raytrace                   | 212 ms                                                 | 162 ms: 1.31x faster                                                 |
| async_tree_memoization_tg  | 323 ms                                                 | 253 ms: 1.28x faster                                                 |
| logging_simple             | 3.69 us                                                | 3.01 us: 1.23x faster                                                |
| async_tree_none            | 266 ms                                                 | 217 ms: 1.23x faster                                                 |
| logging_silent             | 76.4 ns                                                | 62.5 ns: 1.22x faster                                                |
| async_tree_io_tg           | 669 ms                                                 | 555 ms: 1.21x faster                                                 |
| logging_format             | 3.98 us                                                | 3.30 us: 1.21x faster                                                |
| coroutines                 | 19.2 ms                                                | 16.0 ms: 1.20x faster                                                |
| float                      | 55.8 ms                                                | 46.4 ms: 1.20x faster                                                |
| mako                       | 7.71 ms                                                | 6.46 ms: 1.19x faster                                                |
| comprehensions             | 14.5 us                                                | 12.3 us: 1.18x faster                                                |
| async_tree_memoization     | 312 ms                                                 | 268 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed_tg | 532 ms                                                 | 457 ms: 1.17x faster                                                 |
| async_tree_io              | 668 ms                                                 | 580 ms: 1.15x faster                                                 |
| deltablue                  | 2.71 ms                                                | 2.36 ms: 1.15x faster                                                |
| unpickle_pure_python       | 151 us                                                 | 132 us: 1.14x faster                                                 |
| pickle_pure_python         | 200 us                                                 | 176 us: 1.14x faster                                                 |
| spectral_norm              | 76.4 ms                                                | 67.3 ms: 1.14x faster                                                |
| async_tree_cpu_io_mixed    | 526 ms                                                 | 476 ms: 1.10x faster                                                 |
| mdp                        | 1.58 sec                                               | 1.44 sec: 1.10x faster                                               |
| tomli_loads                | 1.39 sec                                               | 1.27 sec: 1.10x faster                                               |
| xml_etree_process          | 39.7 ms                                                | 36.1 ms: 1.10x faster                                                |
| chaos                      | 42.5 ms                                                | 39.0 ms: 1.09x faster                                                |
| nqueens                    | 62.4 ms                                                | 57.3 ms: 1.09x faster                                                |
| nbody                      | 68.8 ms                                                | 63.6 ms: 1.08x faster                                                |
| regex_compile              | 77.9 ms                                                | 72.1 ms: 1.08x faster                                                |
| asyncio_tcp                | 449 ms                                                 | 416 ms: 1.08x faster                                                 |
| scimark_sparse_mat_mult    | 3.14 ms                                                | 2.92 ms: 1.07x faster                                                |
| xml_etree_generate         | 55.8 ms                                                | 52.2 ms: 1.07x faster                                                |
| bench_thread_pool          | 504 us                                                 | 472 us: 1.07x faster                                                 |
| sympy_str                  | 148 ms                                                 | 139 ms: 1.07x faster                                                 |
| sympy_sum                  | 77.6 ms                                                | 73.4 ms: 1.06x faster                                                |
| richards                   | 32.1 ms                                                | 30.4 ms: 1.06x faster                                                |
| sqlglot_normalize          | 186 ms                                                 | 177 ms: 1.05x faster                                                 |
| richards_super             | 36.0 ms                                                | 34.3 ms: 1.05x faster                                                |
| json                       | 3.09 ms                                                | 2.94 ms: 1.05x faster                                                |
| scimark_fft                | 195 ms                                                 | 187 ms: 1.05x faster                                                 |
| pprint_safe_repr           | 497 ms                                                 | 475 ms: 1.05x faster                                                 |
| sympy_integrate            | 11.4 ms                                                | 10.9 ms: 1.04x faster                                                |
| xml_etree_iterparse        | 74.0 ms                                                | 71.3 ms: 1.04x faster                                                |
| pprint_pformat             | 1.01 sec                                               | 976 ms: 1.04x faster                                                 |
| regex_dna                  | 154 ms                                                 | 149 ms: 1.03x faster                                                 |
| scimark_monte_carlo        | 45.0 ms                                                | 43.6 ms: 1.03x faster                                                |
| async_generators           | 304 ms                                                 | 294 ms: 1.03x faster                                                 |
| unpickle_list              | 3.02 us                                                | 2.93 us: 1.03x faster                                                |
| regex_effbot               | 2.64 ms                                                | 2.56 ms: 1.03x faster                                                |
| pathlib                    | 24.2 ms                                                | 23.5 ms: 1.03x faster                                                |
| sqlglot_optimize           | 34.0 ms                                                | 33.1 ms: 1.03x faster                                                |
| sqlglot_transpile          | 1.02 ms                                                | 994 us: 1.03x faster                                                 |
| sqlglot_parse              | 848 us                                                 | 827 us: 1.03x faster                                                 |
| hexiom                     | 4.54 ms                                                | 4.44 ms: 1.02x faster                                                |
| django_template            | 22.3 ms                                                | 21.9 ms: 1.02x faster                                                |
| fannkuch                   | 248 ms                                                 | 244 ms: 1.02x faster                                                 |
| json_loads                 | 17.2 us                                                | 17.0 us: 1.01x faster                                                |
| sympy_expand               | 241 ms                                                 | 239 ms: 1.01x faster                                                 |
| pycparser                  | 677 ms                                                 | 672 ms: 1.01x faster                                                 |
| crypto_pyaes               | 51.9 ms                                                | 51.5 ms: 1.01x faster                                                |
| go                         | 102 ms                                                 | 101 ms: 1.00x faster                                                 |
| meteor_contest             | 71.7 ms                                                | 72.1 ms: 1.00x slower                                                |
| json_dumps                 | 6.22 ms                                                | 6.26 ms: 1.01x slower                                                |
| typing_runtime_protocols   | 93.0 us                                                | 94.1 us: 1.01x slower                                                |
| pidigits                   | 282 ms                                                 | 286 ms: 1.01x slower                                                 |
| unpickle                   | 9.12 us                                                | 9.32 us: 1.02x slower                                                |
| gc_traversal               | 2.40 ms                                                | 2.46 ms: 1.03x slower                                                |
| pickle_dict                | 18.1 us                                                | 18.6 us: 1.03x slower                                                |
| asyncio_tcp_ssl            | 1.24 sec                                               | 1.29 sec: 1.04x slower                                               |
| pickle                     | 7.23 us                                                | 7.49 us: 1.04x slower                                                |
| pickle_list                | 2.89 us                                                | 3.02 us: 1.05x slower                                                |
| scimark_lu                 | 76.0 ms                                                | 80.8 ms: 1.06x slower                                                |
| bench_mp_pool              | 44.9 ms                                                | 48.7 ms: 1.09x slower                                                |
| regex_v8                   | 16.0 ms                                                | 17.4 ms: 1.09x slower                                                |
| scimark_sor                | 87.4 ms                                                | 102 ms: 1.17x slower                                                 |
| coverage                   | 38.9 ms                                                | 46.3 ms: 1.19x slower                                                |
| telco                      | 3.68 ms                                                | 4.55 ms: 1.24x slower                                                |
| create_gc_cycles           | 701 us                                                 | 894 us: 1.27x slower                                                 |
| python_startup             | 11.4 ms                                                | 14.9 ms: 1.31x slower                                                |
| python_startup_no_site     | 9.37 ms                                                | 12.3 ms: 1.31x slower                                                |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                         |

Benchmark hidden because not significant (8): tornado_http, xml_etree_parse, docutils, sqlite_synth, asyncio_websockets, pyflate, 2to3, dask
Ignored benchmarks (8) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-darwin-arm64-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, chameleon, dulwich_log, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (14) of results/bm-20240618-3.14.0a0-a1bdb94-JIT/bm-20240618-darwin-arm64-brandtbucher-no_cold_exits-3.14.0a0-a1bdb94.json: async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, bpe_tokeniser, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.17x