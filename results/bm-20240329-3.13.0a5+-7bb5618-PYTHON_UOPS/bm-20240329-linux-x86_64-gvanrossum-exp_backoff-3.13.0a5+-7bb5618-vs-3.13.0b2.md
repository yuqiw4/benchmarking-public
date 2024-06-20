# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 7bb5618
- commit date: 2024-03-29
- overall geometric mean: 1.14x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 316 ms: 1.15x slower                                              |
| chameleon      | 7.22 ms                                                    | 7.81 ms: 1.08x slower                                             |
| docutils       | 2.83 sec                                                   | 3.13 sec: 1.11x slower                                            |
| html5lib       | 67.2 ms                                                    | 72.2 ms: 1.07x slower                                             |
| tornado_http   | 94.6 ms                                                    | 104 ms: 1.09x slower                                              |
| Geometric mean | (ref)                                                      | 1.10x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 611 ms                                                     | 632 ms: 1.03x slower                                              |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 612 ms: 1.04x slower                                              |
| async_tree_io_tg           | 936 ms                                                     | 984 ms: 1.05x slower                                              |
| async_tree_memoization     | 463 ms                                                     | 487 ms: 1.05x slower                                              |
| async_tree_io              | 939 ms                                                     | 1.01 sec: 1.07x slower                                            |
| async_tree_memoization_tg  | 444 ms                                                     | 482 ms: 1.09x slower                                              |
| async_tree_none_tg         | 336 ms                                                     | 369 ms: 1.10x slower                                              |
| async_tree_none            | 378 ms                                                     | 421 ms: 1.11x slower                                              |
| Geometric mean             | (ref)                                                      | 1.07x slower                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 192 ms: 1.01x slower                                              |
| float          | 78.9 ms                                                    | 99.2 ms: 1.26x slower                                             |
| nbody          | 88.3 ms                                                    | 130 ms: 1.48x slower                                              |
| Geometric mean | (ref)                                                      | 1.23x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.63 ms: 1.01x faster                                             |
| regex_dna      | 221 ms                                                     | 226 ms: 1.02x slower                                              |
| regex_v8       | 25.1 ms                                                    | 26.5 ms: 1.05x slower                                             |
| regex_compile  | 137 ms                                                     | 196 ms: 1.43x slower                                              |
| Geometric mean | (ref)                                                      | 1.11x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.39 us: 1.01x slower                                             |
| pickle_dict          | 34.8 us                                                    | 35.1 us: 1.01x slower                                             |
| json_dumps           | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                             |
| pickle_list          | 5.11 us                                                    | 5.23 us: 1.03x slower                                             |
| unpickle             | 15.1 us                                                    | 15.6 us: 1.03x slower                                             |
| pickle               | 11.5 us                                                    | 12.0 us: 1.05x slower                                             |
| pickle_pure_python   | 305 us                                                     | 322 us: 1.06x slower                                              |
| xml_etree_iterparse  | 107 ms                                                     | 116 ms: 1.08x slower                                              |
| xml_etree_process    | 61.2 ms                                                    | 66.3 ms: 1.08x slower                                             |
| xml_etree_generate   | 87.4 ms                                                    | 98.8 ms: 1.13x slower                                             |
| tomli_loads          | 2.12 sec                                                   | 2.77 sec: 1.31x slower                                            |
| unpickle_pure_python | 218 us                                                     | 316 us: 1.45x slower                                              |
| Geometric mean       | (ref)                                                      | 1.08x slower                                                      |

Benchmark hidden because not significant (2): json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.8 ms: 1.00x slower                                             |
| python_startup_no_site | 7.11 ms                                                    | 9.17 ms: 1.29x slower                                             |
| Geometric mean         | (ref)                                                      | 1.14x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_text     | 23.7 ms                                                    | 27.4 ms: 1.16x slower                                             |
| django_template | 34.8 ms                                                    | 42.2 ms: 1.21x slower                                             |
| mako            | 11.2 ms                                                    | 13.8 ms: 1.23x slower                                             |
| genshi_xml      | 51.6 ms                                                    | 64.2 ms: 1.24x slower                                             |
| Geometric mean  | (ref)                                                      | 1.21x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618 |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 127 us: 1.30x faster                                              |
| create_gc_cycles           | 1.82 ms                                                    | 1.69 ms: 1.07x faster                                             |
| gc_traversal               | 3.98 ms                                                    | 3.74 ms: 1.06x faster                                             |
| regex_effbot               | 3.67 ms                                                    | 3.63 ms: 1.01x faster                                             |
| deepcopy_reduce            | 3.35 us                                                    | 3.31 us: 1.01x faster                                             |
| coroutines                 | 23.2 ms                                                    | 23.0 ms: 1.01x faster                                             |
| python_startup             | 10.8 ms                                                    | 10.8 ms: 1.00x slower                                             |
| asyncio_tcp                | 508 ms                                                     | 510 ms: 1.00x slower                                              |
| asyncio_websockets         | 567 ms                                                     | 570 ms: 1.01x slower                                              |
| pidigits                   | 191 ms                                                     | 192 ms: 1.01x slower                                              |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                             |
| unpickle_list              | 5.34 us                                                    | 5.39 us: 1.01x slower                                             |
| pickle_dict                | 34.8 us                                                    | 35.1 us: 1.01x slower                                             |
| json_dumps                 | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                             |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                            |
| thrift                     | 823 us                                                     | 834 us: 1.01x slower                                              |
| regex_dna                  | 221 ms                                                     | 226 ms: 1.02x slower                                              |
| pickle_list                | 5.11 us                                                    | 5.23 us: 1.03x slower                                             |
| unpickle                   | 15.1 us                                                    | 15.6 us: 1.03x slower                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 632 ms: 1.03x slower                                              |
| json                       | 5.31 ms                                                    | 5.49 ms: 1.03x slower                                             |
| sqlite_synth               | 2.99 us                                                    | 3.09 us: 1.04x slower                                             |
| generators                 | 29.6 ms                                                    | 30.9 ms: 1.04x slower                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 612 ms: 1.04x slower                                              |
| dask                       | 369 ms                                                     | 386 ms: 1.04x slower                                              |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.05x slower                                             |
| djangocms                  | 31.5 us                                                    | 33.1 us: 1.05x slower                                             |
| async_tree_io_tg           | 936 ms                                                     | 984 ms: 1.05x slower                                              |
| async_tree_memoization     | 463 ms                                                     | 487 ms: 1.05x slower                                              |
| regex_v8                   | 25.1 ms                                                    | 26.5 ms: 1.05x slower                                             |
| pickle_pure_python         | 305 us                                                     | 322 us: 1.06x slower                                              |
| coverage                   | 93.1 ms                                                    | 98.5 ms: 1.06x slower                                             |
| deepcopy                   | 367 us                                                     | 392 us: 1.07x slower                                              |
| gunicorn                   | 1.28 ms                                                    | 1.37 ms: 1.07x slower                                             |
| logging_silent             | 105 ns                                                     | 112 ns: 1.07x slower                                              |
| aiohttp                    | 1.18 ms                                                    | 1.26 ms: 1.07x slower                                             |
| async_tree_io              | 939 ms                                                     | 1.01 sec: 1.07x slower                                            |
| html5lib                   | 67.2 ms                                                    | 72.2 ms: 1.07x slower                                             |
| xml_etree_iterparse        | 107 ms                                                     | 116 ms: 1.08x slower                                              |
| chameleon                  | 7.22 ms                                                    | 7.81 ms: 1.08x slower                                             |
| xml_etree_process          | 61.2 ms                                                    | 66.3 ms: 1.08x slower                                             |
| mdp                        | 2.79 sec                                                   | 3.02 sec: 1.08x slower                                            |
| async_tree_memoization_tg  | 444 ms                                                     | 482 ms: 1.09x slower                                              |
| bench_thread_pool          | 834 us                                                     | 910 us: 1.09x slower                                              |
| async_generators           | 442 ms                                                     | 483 ms: 1.09x slower                                              |
| tornado_http               | 94.6 ms                                                    | 104 ms: 1.09x slower                                              |
| async_tree_none_tg         | 336 ms                                                     | 369 ms: 1.10x slower                                              |
| docutils                   | 2.83 sec                                                   | 3.13 sec: 1.11x slower                                            |
| async_tree_none            | 378 ms                                                     | 421 ms: 1.11x slower                                              |
| pylint                     | 317 ms                                                     | 354 ms: 1.12x slower                                              |
| mypy2                      | 742 ms                                                     | 830 ms: 1.12x slower                                              |
| dulwich_log                | 67.2 ms                                                    | 75.5 ms: 1.12x slower                                             |
| xml_etree_generate         | 87.4 ms                                                    | 98.8 ms: 1.13x slower                                             |
| logging_format             | 6.47 us                                                    | 7.36 us: 1.14x slower                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.04 ms: 1.15x slower                                             |
| telco                      | 8.41 ms                                                    | 9.69 ms: 1.15x slower                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.89 ms: 1.15x slower                                             |
| 2to3                       | 274 ms                                                     | 316 ms: 1.15x slower                                              |
| genshi_text                | 23.7 ms                                                    | 27.4 ms: 1.16x slower                                             |
| meteor_contest             | 110 ms                                                     | 128 ms: 1.16x slower                                              |
| scimark_fft                | 392 ms                                                     | 457 ms: 1.16x slower                                              |
| sympy_sum                  | 156 ms                                                     | 182 ms: 1.17x slower                                              |
| sympy_integrate            | 20.5 ms                                                    | 24.0 ms: 1.17x slower                                             |
| logging_simple             | 5.74 us                                                    | 6.75 us: 1.17x slower                                             |
| sympy_expand               | 473 ms                                                     | 556 ms: 1.18x slower                                              |
| sqlglot_parse              | 1.32 ms                                                    | 1.56 ms: 1.18x slower                                             |
| sqlglot_normalize          | 110 ms                                                     | 130 ms: 1.18x slower                                              |
| sympy_str                  | 282 ms                                                     | 335 ms: 1.19x slower                                              |
| pathlib                    | 17.3 ms                                                    | 20.7 ms: 1.20x slower                                             |
| sqlglot_optimize           | 55.5 ms                                                    | 66.9 ms: 1.20x slower                                             |
| django_template            | 34.8 ms                                                    | 42.2 ms: 1.21x slower                                             |
| crypto_pyaes               | 77.5 ms                                                    | 94.4 ms: 1.22x slower                                             |
| mako                       | 11.2 ms                                                    | 13.8 ms: 1.23x slower                                             |
| pycparser                  | 1.16 sec                                                   | 1.43 sec: 1.23x slower                                            |
| genshi_xml                 | 51.6 ms                                                    | 64.2 ms: 1.24x slower                                             |
| deepcopy_memo              | 39.7 us                                                    | 49.5 us: 1.25x slower                                             |
| float                      | 78.9 ms                                                    | 99.2 ms: 1.26x slower                                             |
| fannkuch                   | 402 ms                                                     | 513 ms: 1.28x slower                                              |
| python_startup_no_site     | 7.11 ms                                                    | 9.17 ms: 1.29x slower                                             |
| richards_super             | 57.4 ms                                                    | 74.4 ms: 1.30x slower                                             |
| spectral_norm              | 116 ms                                                     | 151 ms: 1.30x slower                                              |
| tomli_loads                | 2.12 sec                                                   | 2.77 sec: 1.31x slower                                            |
| richards                   | 50.9 ms                                                    | 67.1 ms: 1.32x slower                                             |
| go                         | 145 ms                                                     | 193 ms: 1.34x slower                                              |
| chaos                      | 61.3 ms                                                    | 82.5 ms: 1.35x slower                                             |
| scimark_sor                | 127 ms                                                     | 173 ms: 1.35x slower                                              |
| scimark_monte_carlo        | 69.2 ms                                                    | 94.1 ms: 1.36x slower                                             |
| pprint_safe_repr           | 758 ms                                                     | 1.03 sec: 1.36x slower                                            |
| scimark_lu                 | 122 ms                                                     | 167 ms: 1.37x slower                                              |
| pyflate                    | 484 ms                                                     | 670 ms: 1.38x slower                                              |
| pprint_pformat             | 1.56 sec                                                   | 2.17 sec: 1.40x slower                                            |
| regex_compile              | 137 ms                                                     | 196 ms: 1.43x slower                                              |
| deltablue                  | 3.25 ms                                                    | 4.66 ms: 1.43x slower                                             |
| unpickle_pure_python       | 218 us                                                     | 316 us: 1.45x slower                                              |
| raytrace                   | 267 ms                                                     | 391 ms: 1.47x slower                                              |
| nbody                      | 88.3 ms                                                    | 130 ms: 1.48x slower                                              |
| comprehensions             | 16.6 us                                                    | 24.7 us: 1.49x slower                                             |
| nqueens                    | 81.4 ms                                                    | 124 ms: 1.53x slower                                              |
| hexiom                     | 6.30 ms                                                    | 10.4 ms: 1.65x slower                                             |
| Geometric mean             | (ref)                                                      | 1.14x slower                                                      |

Benchmark hidden because not significant (2): json_loads, xml_etree_parse
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-7bb5618-PYTHON_UOPS/bm-20240329-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-7bb5618.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 0.98x