# Results vs. 3.13.0b2

- fork: python
- ref: 48c0b05cf0dd2db275bd
- machine: linux-x86_64
- commit hash: 48c0b05
- commit date: 2024-03-26
- overall geometric mean: 1.01x slower
- HPT reliability: 99.58%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-python-48c0b05cf0dd2db275bd-3.13.0a5+-48c0b05 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 276 ms: 1.01x slower                                                   |
| chameleon      | 7.22 ms                                                    | 6.88 ms: 1.05x faster                                                  |
| docutils       | 2.83 sec                                                   | 2.90 sec: 1.03x slower                                                 |
| html5lib       | 67.2 ms                                                    | 67.8 ms: 1.01x slower                                                  |
| tornado_http   | 94.6 ms                                                    | 96.8 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-python-48c0b05cf0dd2db275bd-3.13.0a5+-48c0b05 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 354 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 602 ms: 1.03x slower                                                   |
| async_tree_none_tg         | 336 ms                                                     | 350 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (5): async_tree_memoization, async_tree_io_tg, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-python-48c0b05cf0dd2db275bd-3.13.0a5+-48c0b05 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 76.7 ms: 1.03x faster                                                  |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                   |
| nbody          | 88.3 ms                                                    | 92.7 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-python-48c0b05cf0dd2db275bd-3.13.0a5+-48c0b05 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 221 ms                                                     | 217 ms: 1.02x faster                                                   |
| regex_v8       | 25.1 ms                                                    | 25.3 ms: 1.01x slower                                                  |
| regex_effbot   | 3.67 ms                                                    | 3.75 ms: 1.02x slower                                                  |
| regex_compile  | 137 ms                                                     | 147 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                      | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-python-48c0b05cf0dd2db275bd-3.13.0a5+-48c0b05 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_list          | 5.11 us                                                    | 4.94 us: 1.03x faster                                                  |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.03x faster                                                  |
| xml_etree_process    | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.09 sec: 1.02x faster                                                 |
| pickle_dict          | 34.8 us                                                    | 34.3 us: 1.01x faster                                                  |
| json_loads           | 28.9 us                                                    | 28.6 us: 1.01x faster                                                  |
| unpickle_list        | 5.34 us                                                    | 5.29 us: 1.01x faster                                                  |
| xml_etree_generate   | 87.4 ms                                                    | 87.0 ms: 1.00x faster                                                  |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                  |
| unpickle_pure_python | 218 us                                                     | 241 us: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                           |

Benchmark hidden because not significant (4): xml_etree_parse, xml_etree_iterparse, unpickle, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-python-48c0b05cf0dd2db275bd-3.13.0a5+-48c0b05 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                                  |
| python_startup_no_site | 7.11 ms                                                    | 9.48 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-python-48c0b05cf0dd2db275bd-3.13.0a5+-48c0b05 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                  |
| genshi_text     | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                                  |
| django_template | 34.8 ms                                                    | 36.1 ms: 1.04x slower                                                  |
| genshi_xml      | 51.6 ms                                                    | 54.3 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-python-48c0b05cf0dd2db275bd-3.13.0a5+-48c0b05 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 111 us: 1.48x faster                                                   |
| scimark_fft                | 392 ms                                                     | 351 ms: 1.12x faster                                                   |
| richards_super             | 57.4 ms                                                    | 52.6 ms: 1.09x faster                                                  |
| richards                   | 50.9 ms                                                    | 46.7 ms: 1.09x faster                                                  |
| create_gc_cycles           | 1.82 ms                                                    | 1.67 ms: 1.09x faster                                                  |
| gc_traversal               | 3.98 ms                                                    | 3.69 ms: 1.08x faster                                                  |
| async_tree_none            | 378 ms                                                     | 354 ms: 1.07x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                    | 3.17 us: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.02 ms: 1.05x faster                                                  |
| mdp                        | 2.79 sec                                                   | 2.65 sec: 1.05x faster                                                 |
| chameleon                  | 7.22 ms                                                    | 6.88 ms: 1.05x faster                                                  |
| sqlite_synth               | 2.99 us                                                    | 2.88 us: 1.04x faster                                                  |
| mako                       | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                  |
| pickle_list                | 5.11 us                                                    | 4.94 us: 1.03x faster                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 75.0 ms: 1.03x faster                                                  |
| pprint_pformat             | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                 |
| float                      | 78.9 ms                                                    | 76.7 ms: 1.03x faster                                                  |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.03x faster                                                  |
| spectral_norm              | 116 ms                                                     | 114 ms: 1.02x faster                                                   |
| deepcopy                   | 367 us                                                     | 360 us: 1.02x faster                                                   |
| xml_etree_process          | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                  |
| regex_dna                  | 221 ms                                                     | 217 ms: 1.02x faster                                                   |
| thrift                     | 823 us                                                     | 810 us: 1.02x faster                                                   |
| tomli_loads                | 2.12 sec                                                   | 2.09 sec: 1.02x faster                                                 |
| pickle_dict                | 34.8 us                                                    | 34.3 us: 1.01x faster                                                  |
| fannkuch                   | 402 ms                                                     | 396 ms: 1.01x faster                                                   |
| json_loads                 | 28.9 us                                                    | 28.6 us: 1.01x faster                                                  |
| logging_silent             | 105 ns                                                     | 104 ns: 1.01x faster                                                   |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                   |
| unpickle_list              | 5.34 us                                                    | 5.29 us: 1.01x faster                                                  |
| generators                 | 29.6 ms                                                    | 29.5 ms: 1.01x faster                                                  |
| deepcopy_memo              | 39.7 us                                                    | 39.5 us: 1.00x faster                                                  |
| xml_etree_generate         | 87.4 ms                                                    | 87.0 ms: 1.00x faster                                                  |
| asyncio_tcp                | 508 ms                                                     | 510 ms: 1.00x slower                                                   |
| asyncio_websockets         | 567 ms                                                     | 569 ms: 1.00x slower                                                   |
| sqlglot_transpile          | 1.63 ms                                                    | 1.64 ms: 1.01x slower                                                  |
| 2to3                       | 274 ms                                                     | 276 ms: 1.01x slower                                                   |
| regex_v8                   | 25.1 ms                                                    | 25.3 ms: 1.01x slower                                                  |
| html5lib                   | 67.2 ms                                                    | 67.8 ms: 1.01x slower                                                  |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                 |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                  |
| json                       | 5.31 ms                                                    | 5.37 ms: 1.01x slower                                                  |
| pycparser                  | 1.16 sec                                                   | 1.17 sec: 1.01x slower                                                 |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                   |
| logging_format             | 6.47 us                                                    | 6.57 us: 1.02x slower                                                  |
| pyflate                    | 484 ms                                                     | 493 ms: 1.02x slower                                                   |
| dask                       | 369 ms                                                     | 377 ms: 1.02x slower                                                   |
| regex_effbot               | 3.67 ms                                                    | 3.75 ms: 1.02x slower                                                  |
| bench_thread_pool          | 834 us                                                     | 852 us: 1.02x slower                                                   |
| tornado_http               | 94.6 ms                                                    | 96.8 ms: 1.02x slower                                                  |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 602 ms: 1.03x slower                                                   |
| docutils                   | 2.83 sec                                                   | 2.90 sec: 1.03x slower                                                 |
| scimark_monte_carlo        | 69.2 ms                                                    | 71.0 ms: 1.03x slower                                                  |
| gunicorn                   | 1.28 ms                                                    | 1.31 ms: 1.03x slower                                                  |
| sqlglot_normalize          | 110 ms                                                     | 113 ms: 1.03x slower                                                   |
| genshi_text                | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                                  |
| scimark_sor                | 127 ms                                                     | 131 ms: 1.03x slower                                                   |
| python_startup             | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                                  |
| djangocms                  | 31.5 us                                                    | 32.4 us: 1.03x slower                                                  |
| chaos                      | 61.3 ms                                                    | 63.1 ms: 1.03x slower                                                  |
| sympy_str                  | 282 ms                                                     | 291 ms: 1.03x slower                                                   |
| telco                      | 8.41 ms                                                    | 8.69 ms: 1.03x slower                                                  |
| coverage                   | 93.1 ms                                                    | 96.4 ms: 1.04x slower                                                  |
| django_template            | 34.8 ms                                                    | 36.1 ms: 1.04x slower                                                  |
| logging_simple             | 5.74 us                                                    | 5.96 us: 1.04x slower                                                  |
| sympy_expand               | 473 ms                                                     | 491 ms: 1.04x slower                                                   |
| async_tree_none_tg         | 336 ms                                                     | 350 ms: 1.04x slower                                                   |
| async_generators           | 442 ms                                                     | 463 ms: 1.05x slower                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 58.1 ms: 1.05x slower                                                  |
| nbody                      | 88.3 ms                                                    | 92.7 ms: 1.05x slower                                                  |
| genshi_xml                 | 51.6 ms                                                    | 54.3 ms: 1.05x slower                                                  |
| dulwich_log                | 67.2 ms                                                    | 70.9 ms: 1.06x slower                                                  |
| sympy_sum                  | 156 ms                                                     | 165 ms: 1.06x slower                                                   |
| deltablue                  | 3.25 ms                                                    | 3.44 ms: 1.06x slower                                                  |
| sympy_integrate            | 20.5 ms                                                    | 21.8 ms: 1.06x slower                                                  |
| mypy2                      | 742 ms                                                     | 789 ms: 1.06x slower                                                   |
| regex_compile              | 137 ms                                                     | 147 ms: 1.07x slower                                                   |
| go                         | 145 ms                                                     | 155 ms: 1.08x slower                                                   |
| raytrace                   | 267 ms                                                     | 289 ms: 1.08x slower                                                   |
| pathlib                    | 17.3 ms                                                    | 19.0 ms: 1.09x slower                                                  |
| scimark_lu                 | 122 ms                                                     | 134 ms: 1.10x slower                                                   |
| unpickle_pure_python       | 218 us                                                     | 241 us: 1.10x slower                                                   |
| nqueens                    | 81.4 ms                                                    | 90.1 ms: 1.11x slower                                                  |
| comprehensions             | 16.6 us                                                    | 18.4 us: 1.11x slower                                                  |
| hexiom                     | 6.30 ms                                                    | 7.23 ms: 1.15x slower                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 9.48 ms: 1.33x slower                                                  |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (14): async_tree_memoization, async_tree_io_tg, async_tree_io, coroutines, pprint_safe_repr, xml_etree_parse, xml_etree_iterparse, sqlglot_parse, unpickle, pickle_pure_python, bench_mp_pool, async_tree_cpu_io_mixed, async_tree_memoization_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240326-3.13.0a5+-48c0b05-JIT/bm-20240326-linux-x86_64-python-48c0b05cf0dd2db275bd-3.13.0a5+-48c0b05.json: unpack_sequence

# HPT report

- Reliability score: 99.58% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.05x