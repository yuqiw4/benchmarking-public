# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 7bb5618
- commit date: 2024-03-29
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 281 ms: 1.02x slower                                              |
| chameleon      | 7.22 ms                                                    | 7.19 ms: 1.00x faster                                             |
| docutils       | 2.83 sec                                                   | 2.90 sec: 1.02x slower                                            |
| html5lib       | 67.2 ms                                                    | 66.8 ms: 1.01x faster                                             |
| tornado_http   | 94.6 ms                                                    | 97.1 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                      | 1.01x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|--------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none_tg | 336 ms                                                     | 342 ms: 1.02x slower                                              |
| async_tree_none    | 378 ms                                                     | 391 ms: 1.03x slower                                              |
| Geometric mean     | (ref)                                                      | 1.01x slower                                                      |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.1 ms: 1.02x faster                                             |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                              |
| nbody          | 88.3 ms                                                    | 90.6 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                      | 1.00x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                             |
| regex_dna      | 221 ms                                                     | 230 ms: 1.04x slower                                              |
| regex_effbot   | 3.67 ms                                                    | 3.84 ms: 1.05x slower                                             |
| regex_compile  | 137 ms                                                     | 146 ms: 1.07x slower                                              |
| Geometric mean | (ref)                                                      | 1.05x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_list          | 5.11 us                                                    | 4.93 us: 1.04x faster                                             |
| tomli_loads          | 2.12 sec                                                   | 2.07 sec: 1.03x faster                                            |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                             |
| json_loads           | 28.9 us                                                    | 28.6 us: 1.01x faster                                             |
| pickle_dict          | 34.8 us                                                    | 34.6 us: 1.01x faster                                             |
| unpickle_list        | 5.34 us                                                    | 5.38 us: 1.01x slower                                             |
| xml_etree_process    | 61.2 ms                                                    | 61.7 ms: 1.01x slower                                             |
| pickle_pure_python   | 305 us                                                     | 308 us: 1.01x slower                                              |
| xml_etree_generate   | 87.4 ms                                                    | 89.7 ms: 1.03x slower                                             |
| unpickle             | 15.1 us                                                    | 15.7 us: 1.03x slower                                             |
| pickle               | 11.5 us                                                    | 12.0 us: 1.04x slower                                             |
| unpickle_pure_python | 218 us                                                     | 245 us: 1.13x slower                                              |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                      |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                             |
| python_startup_no_site | 7.11 ms                                                    | 9.49 ms: 1.34x slower                                             |
| Geometric mean         | (ref)                                                      | 1.17x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                             |
| django_template | 34.8 ms                                                    | 36.5 ms: 1.05x slower                                             |
| genshi_text     | 23.7 ms                                                    | 25.4 ms: 1.07x slower                                             |
| genshi_xml      | 51.6 ms                                                    | 56.4 ms: 1.09x slower                                             |
| Geometric mean  | (ref)                                                      | 1.04x slower                                                      |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|--------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 117 us: 1.41x faster                                              |
| scimark_fft              | 392 ms                                                     | 346 ms: 1.14x faster                                              |
| create_gc_cycles         | 1.82 ms                                                    | 1.69 ms: 1.08x faster                                             |
| richards                 | 50.9 ms                                                    | 47.3 ms: 1.08x faster                                             |
| richards_super           | 57.4 ms                                                    | 53.9 ms: 1.06x faster                                             |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.96 ms: 1.06x faster                                             |
| gc_traversal             | 3.98 ms                                                    | 3.78 ms: 1.05x faster                                             |
| mako                     | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                             |
| mdp                      | 2.79 sec                                                   | 2.67 sec: 1.04x faster                                            |
| deepcopy_reduce          | 3.35 us                                                    | 3.21 us: 1.04x faster                                             |
| crypto_pyaes             | 77.5 ms                                                    | 74.6 ms: 1.04x faster                                             |
| pickle_list              | 5.11 us                                                    | 4.93 us: 1.04x faster                                             |
| sqlite_synth             | 2.99 us                                                    | 2.89 us: 1.03x faster                                             |
| coroutines               | 23.2 ms                                                    | 22.4 ms: 1.03x faster                                             |
| tomli_loads              | 2.12 sec                                                   | 2.07 sec: 1.03x faster                                            |
| float                    | 78.9 ms                                                    | 77.1 ms: 1.02x faster                                             |
| json_dumps               | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                             |
| thrift                   | 823 us                                                     | 810 us: 1.02x faster                                              |
| deepcopy                 | 367 us                                                     | 361 us: 1.02x faster                                              |
| fannkuch                 | 402 ms                                                     | 396 ms: 1.01x faster                                              |
| json_loads               | 28.9 us                                                    | 28.6 us: 1.01x faster                                             |
| pidigits                 | 191 ms                                                     | 189 ms: 1.01x faster                                              |
| pprint_pformat           | 1.56 sec                                                   | 1.55 sec: 1.01x faster                                            |
| html5lib                 | 67.2 ms                                                    | 66.8 ms: 1.01x faster                                             |
| pickle_dict              | 34.8 us                                                    | 34.6 us: 1.01x faster                                             |
| chameleon                | 7.22 ms                                                    | 7.19 ms: 1.00x faster                                             |
| spectral_norm            | 116 ms                                                     | 116 ms: 1.00x faster                                              |
| asyncio_tcp              | 508 ms                                                     | 511 ms: 1.01x slower                                              |
| unpickle_list            | 5.34 us                                                    | 5.38 us: 1.01x slower                                             |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.85 sec: 1.01x slower                                            |
| xml_etree_process        | 61.2 ms                                                    | 61.7 ms: 1.01x slower                                             |
| pickle_pure_python       | 305 us                                                     | 308 us: 1.01x slower                                              |
| json                     | 5.31 ms                                                    | 5.36 ms: 1.01x slower                                             |
| meteor_contest           | 110 ms                                                     | 111 ms: 1.01x slower                                              |
| sqlglot_transpile        | 1.63 ms                                                    | 1.66 ms: 1.01x slower                                             |
| generators               | 29.6 ms                                                    | 30.1 ms: 1.02x slower                                             |
| djangocms                | 31.5 us                                                    | 32.0 us: 1.02x slower                                             |
| pyflate                  | 484 ms                                                     | 492 ms: 1.02x slower                                              |
| async_tree_none_tg       | 336 ms                                                     | 342 ms: 1.02x slower                                              |
| sqlglot_parse            | 1.32 ms                                                    | 1.35 ms: 1.02x slower                                             |
| logging_format           | 6.47 us                                                    | 6.61 us: 1.02x slower                                             |
| gunicorn                 | 1.28 ms                                                    | 1.31 ms: 1.02x slower                                             |
| dask                     | 369 ms                                                     | 378 ms: 1.02x slower                                              |
| docutils                 | 2.83 sec                                                   | 2.90 sec: 1.02x slower                                            |
| 2to3                     | 274 ms                                                     | 281 ms: 1.02x slower                                              |
| tornado_http             | 94.6 ms                                                    | 97.1 ms: 1.03x slower                                             |
| xml_etree_generate       | 87.4 ms                                                    | 89.7 ms: 1.03x slower                                             |
| nbody                    | 88.3 ms                                                    | 90.6 ms: 1.03x slower                                             |
| bench_thread_pool        | 834 us                                                     | 856 us: 1.03x slower                                              |
| regex_v8                 | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                             |
| python_startup           | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                             |
| aiohttp                  | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                             |
| scimark_monte_carlo      | 69.2 ms                                                    | 71.2 ms: 1.03x slower                                             |
| logging_silent           | 105 ns                                                     | 108 ns: 1.03x slower                                              |
| async_tree_none          | 378 ms                                                     | 391 ms: 1.03x slower                                              |
| sqlglot_normalize        | 110 ms                                                     | 114 ms: 1.03x slower                                              |
| telco                    | 8.41 ms                                                    | 8.71 ms: 1.03x slower                                             |
| unpickle                 | 15.1 us                                                    | 15.7 us: 1.03x slower                                             |
| sympy_str                | 282 ms                                                     | 292 ms: 1.04x slower                                              |
| logging_simple           | 5.74 us                                                    | 5.98 us: 1.04x slower                                             |
| regex_dna                | 221 ms                                                     | 230 ms: 1.04x slower                                              |
| scimark_sor              | 127 ms                                                     | 133 ms: 1.04x slower                                              |
| pickle                   | 11.5 us                                                    | 12.0 us: 1.04x slower                                             |
| sqlglot_optimize         | 55.5 ms                                                    | 58.0 ms: 1.04x slower                                             |
| regex_effbot             | 3.67 ms                                                    | 3.84 ms: 1.05x slower                                             |
| django_template          | 34.8 ms                                                    | 36.5 ms: 1.05x slower                                             |
| dulwich_log              | 67.2 ms                                                    | 70.7 ms: 1.05x slower                                             |
| sympy_expand             | 473 ms                                                     | 498 ms: 1.05x slower                                              |
| async_generators         | 442 ms                                                     | 466 ms: 1.05x slower                                              |
| go                       | 145 ms                                                     | 153 ms: 1.06x slower                                              |
| pycparser                | 1.16 sec                                                   | 1.23 sec: 1.06x slower                                            |
| sympy_sum                | 156 ms                                                     | 166 ms: 1.07x slower                                              |
| sympy_integrate          | 20.5 ms                                                    | 21.9 ms: 1.07x slower                                             |
| regex_compile            | 137 ms                                                     | 146 ms: 1.07x slower                                              |
| mypy2                    | 742 ms                                                     | 791 ms: 1.07x slower                                              |
| coverage                 | 93.1 ms                                                    | 99.8 ms: 1.07x slower                                             |
| chaos                    | 61.3 ms                                                    | 65.8 ms: 1.07x slower                                             |
| genshi_text              | 23.7 ms                                                    | 25.4 ms: 1.07x slower                                             |
| scimark_lu               | 122 ms                                                     | 133 ms: 1.09x slower                                              |
| genshi_xml               | 51.6 ms                                                    | 56.4 ms: 1.09x slower                                             |
| comprehensions           | 16.6 us                                                    | 18.3 us: 1.10x slower                                             |
| pathlib                  | 17.3 ms                                                    | 19.1 ms: 1.10x slower                                             |
| raytrace                 | 267 ms                                                     | 297 ms: 1.11x slower                                              |
| nqueens                  | 81.4 ms                                                    | 90.7 ms: 1.11x slower                                             |
| unpickle_pure_python     | 218 us                                                     | 245 us: 1.13x slower                                              |
| hexiom                   | 6.30 ms                                                    | 7.15 ms: 1.14x slower                                             |
| deltablue                | 3.25 ms                                                    | 3.93 ms: 1.21x slower                                             |
| python_startup_no_site   | 7.11 ms                                                    | 9.49 ms: 1.34x slower                                             |
| Geometric mean           | (ref)                                                      | 1.02x slower                                                      |

Benchmark hidden because not significant (13): async_tree_cpu_io_mixed, async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed_tg, deepcopy_memo, pprint_safe_repr, xml_etree_parse, xml_etree_iterparse, asyncio_websockets, bench_mp_pool, async_tree_io, async_tree_memoization_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-7bb5618-JIT/bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.05x