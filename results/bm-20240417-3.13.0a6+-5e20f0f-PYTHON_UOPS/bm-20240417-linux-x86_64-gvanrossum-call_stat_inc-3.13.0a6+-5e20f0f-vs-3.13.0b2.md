# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 5e20f0f
- commit date: 2024-04-17
- overall geometric mean: 1.23x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 332 ms: 1.21x slower                                                |
| chameleon      | 7.22 ms                                                    | 8.07 ms: 1.12x slower                                               |
| docutils       | 2.83 sec                                                   | 3.28 sec: 1.16x slower                                              |
| html5lib       | 67.2 ms                                                    | 75.6 ms: 1.12x slower                                               |
| tornado_http   | 94.6 ms                                                    | 104 ms: 1.10x slower                                                |
| Geometric mean | (ref)                                                      | 1.14x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 400 ms: 1.06x slower                                                |
| async_tree_io              | 939 ms                                                     | 995 ms: 1.06x slower                                                |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 660 ms: 1.08x slower                                                |
| async_tree_io_tg           | 936 ms                                                     | 1.01 sec: 1.08x slower                                              |
| async_tree_memoization_tg  | 444 ms                                                     | 480 ms: 1.08x slower                                                |
| async_tree_none_tg         | 336 ms                                                     | 371 ms: 1.10x slower                                                |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 649 ms: 1.10x slower                                                |
| async_tree_memoization     | 463 ms                                                     | 529 ms: 1.14x slower                                                |
| Geometric mean             | (ref)                                                      | 1.09x slower                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 195 ms: 1.02x slower                                                |
| float          | 78.9 ms                                                    | 139 ms: 1.76x slower                                                |
| nbody          | 88.3 ms                                                    | 203 ms: 2.30x slower                                                |
| Geometric mean | (ref)                                                      | 1.61x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.88 ms: 1.06x slower                                               |
| regex_dna      | 221 ms                                                     | 235 ms: 1.06x slower                                                |
| regex_v8       | 25.1 ms                                                    | 27.2 ms: 1.08x slower                                               |
| regex_compile  | 137 ms                                                     | 223 ms: 1.63x slower                                                |
| Geometric mean | (ref)                                                      | 1.19x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.9 us: 1.04x faster                                               |
| unpickle_list        | 5.34 us                                                    | 5.24 us: 1.02x faster                                               |
| pickle_list          | 5.11 us                                                    | 5.20 us: 1.02x slower                                               |
| pickle_dict          | 34.8 us                                                    | 35.8 us: 1.03x slower                                               |
| pickle_pure_python   | 305 us                                                     | 314 us: 1.03x slower                                                |
| pickle               | 11.5 us                                                    | 12.1 us: 1.06x slower                                               |
| unpickle             | 15.1 us                                                    | 16.8 us: 1.11x slower                                               |
| xml_etree_process    | 61.2 ms                                                    | 70.4 ms: 1.15x slower                                               |
| xml_etree_generate   | 87.4 ms                                                    | 105 ms: 1.20x slower                                                |
| xml_etree_iterparse  | 107 ms                                                     | 133 ms: 1.24x slower                                                |
| tomli_loads          | 2.12 sec                                                   | 3.41 sec: 1.61x slower                                              |
| unpickle_pure_python | 218 us                                                     | 406 us: 1.86x slower                                                |
| Geometric mean       | (ref)                                                      | 1.14x slower                                                        |

Benchmark hidden because not significant (2): json_dumps, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                               |
| python_startup_no_site | 7.11 ms                                                    | 7.13 ms: 1.00x slower                                               |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_text     | 23.7 ms                                                    | 27.3 ms: 1.15x slower                                               |
| django_template | 34.8 ms                                                    | 42.9 ms: 1.23x slower                                               |
| genshi_xml      | 51.6 ms                                                    | 64.7 ms: 1.25x slower                                               |
| mako            | 11.2 ms                                                    | 20.9 ms: 1.86x slower                                               |
| Geometric mean  | (ref)                                                      | 1.35x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 130 us: 1.27x faster                                                |
| json_loads                 | 28.9 us                                                    | 27.9 us: 1.04x faster                                               |
| create_gc_cycles           | 1.82 ms                                                    | 1.77 ms: 1.03x faster                                               |
| unpickle_list              | 5.34 us                                                    | 5.24 us: 1.02x faster                                               |
| json                       | 5.31 ms                                                    | 5.20 ms: 1.02x faster                                               |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                               |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                               |
| gc_traversal               | 3.98 ms                                                    | 3.95 ms: 1.01x faster                                               |
| python_startup_no_site     | 7.11 ms                                                    | 7.13 ms: 1.00x slower                                               |
| generators                 | 29.6 ms                                                    | 29.7 ms: 1.00x slower                                               |
| asyncio_tcp                | 508 ms                                                     | 513 ms: 1.01x slower                                                |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                              |
| pickle_list                | 5.11 us                                                    | 5.20 us: 1.02x slower                                               |
| pidigits                   | 191 ms                                                     | 195 ms: 1.02x slower                                                |
| deepcopy_reduce            | 3.35 us                                                    | 3.41 us: 1.02x slower                                               |
| thrift                     | 823 us                                                     | 846 us: 1.03x slower                                                |
| pickle_dict                | 34.8 us                                                    | 35.8 us: 1.03x slower                                               |
| pickle_pure_python         | 305 us                                                     | 314 us: 1.03x slower                                                |
| logging_silent             | 105 ns                                                     | 109 ns: 1.05x slower                                                |
| dask                       | 369 ms                                                     | 388 ms: 1.05x slower                                                |
| pickle                     | 11.5 us                                                    | 12.1 us: 1.06x slower                                               |
| sqlite_synth               | 2.99 us                                                    | 3.16 us: 1.06x slower                                               |
| async_tree_none            | 378 ms                                                     | 400 ms: 1.06x slower                                                |
| regex_effbot               | 3.67 ms                                                    | 3.88 ms: 1.06x slower                                               |
| async_tree_io              | 939 ms                                                     | 995 ms: 1.06x slower                                                |
| regex_dna                  | 221 ms                                                     | 235 ms: 1.06x slower                                                |
| gunicorn                   | 1.28 ms                                                    | 1.36 ms: 1.06x slower                                               |
| coverage                   | 93.1 ms                                                    | 99.3 ms: 1.07x slower                                               |
| aiohttp                    | 1.18 ms                                                    | 1.26 ms: 1.07x slower                                               |
| mdp                        | 2.79 sec                                                   | 2.99 sec: 1.07x slower                                              |
| deepcopy                   | 367 us                                                     | 395 us: 1.08x slower                                                |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 660 ms: 1.08x slower                                                |
| async_tree_io_tg           | 936 ms                                                     | 1.01 sec: 1.08x slower                                              |
| async_tree_memoization_tg  | 444 ms                                                     | 480 ms: 1.08x slower                                                |
| regex_v8                   | 25.1 ms                                                    | 27.2 ms: 1.08x slower                                               |
| pathlib                    | 17.3 ms                                                    | 18.8 ms: 1.08x slower                                               |
| tornado_http               | 94.6 ms                                                    | 104 ms: 1.10x slower                                                |
| async_tree_none_tg         | 336 ms                                                     | 371 ms: 1.10x slower                                                |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 649 ms: 1.10x slower                                                |
| unpickle                   | 15.1 us                                                    | 16.8 us: 1.11x slower                                               |
| chameleon                  | 7.22 ms                                                    | 8.07 ms: 1.12x slower                                               |
| bench_thread_pool          | 834 us                                                     | 933 us: 1.12x slower                                                |
| mypy2                      | 742 ms                                                     | 833 ms: 1.12x slower                                                |
| html5lib                   | 67.2 ms                                                    | 75.6 ms: 1.12x slower                                               |
| dulwich_log                | 67.2 ms                                                    | 75.8 ms: 1.13x slower                                               |
| pylint                     | 317 ms                                                     | 360 ms: 1.13x slower                                                |
| async_tree_memoization     | 463 ms                                                     | 529 ms: 1.14x slower                                                |
| async_generators           | 442 ms                                                     | 507 ms: 1.15x slower                                                |
| logging_format             | 6.47 us                                                    | 7.42 us: 1.15x slower                                               |
| xml_etree_process          | 61.2 ms                                                    | 70.4 ms: 1.15x slower                                               |
| telco                      | 8.41 ms                                                    | 9.71 ms: 1.15x slower                                               |
| genshi_text                | 23.7 ms                                                    | 27.3 ms: 1.15x slower                                               |
| docutils                   | 2.83 sec                                                   | 3.28 sec: 1.16x slower                                              |
| logging_simple             | 5.74 us                                                    | 6.72 us: 1.17x slower                                               |
| sympy_expand               | 473 ms                                                     | 562 ms: 1.19x slower                                                |
| pycparser                  | 1.16 sec                                                   | 1.39 sec: 1.20x slower                                              |
| xml_etree_generate         | 87.4 ms                                                    | 105 ms: 1.20x slower                                                |
| sqlglot_transpile          | 1.63 ms                                                    | 1.97 ms: 1.21x slower                                               |
| 2to3                       | 274 ms                                                     | 332 ms: 1.21x slower                                                |
| sqlglot_normalize          | 110 ms                                                     | 134 ms: 1.21x slower                                                |
| sympy_sum                  | 156 ms                                                     | 192 ms: 1.23x slower                                                |
| sqlglot_parse              | 1.32 ms                                                    | 1.63 ms: 1.23x slower                                               |
| django_template            | 34.8 ms                                                    | 42.9 ms: 1.23x slower                                               |
| sympy_str                  | 282 ms                                                     | 349 ms: 1.24x slower                                                |
| xml_etree_iterparse        | 107 ms                                                     | 133 ms: 1.24x slower                                                |
| sympy_integrate            | 20.5 ms                                                    | 25.5 ms: 1.24x slower                                               |
| genshi_xml                 | 51.6 ms                                                    | 64.7 ms: 1.25x slower                                               |
| deepcopy_memo              | 39.7 us                                                    | 50.5 us: 1.27x slower                                               |
| sqlglot_optimize           | 55.5 ms                                                    | 71.1 ms: 1.28x slower                                               |
| meteor_contest             | 110 ms                                                     | 144 ms: 1.31x slower                                                |
| scimark_sor                | 127 ms                                                     | 174 ms: 1.36x slower                                                |
| raytrace                   | 267 ms                                                     | 374 ms: 1.40x slower                                                |
| richards_super             | 57.4 ms                                                    | 81.1 ms: 1.41x slower                                               |
| richards                   | 50.9 ms                                                    | 74.5 ms: 1.46x slower                                               |
| deltablue                  | 3.25 ms                                                    | 4.94 ms: 1.52x slower                                               |
| go                         | 145 ms                                                     | 226 ms: 1.56x slower                                                |
| scimark_fft                | 392 ms                                                     | 630 ms: 1.61x slower                                                |
| tomli_loads                | 2.12 sec                                                   | 3.41 sec: 1.61x slower                                              |
| regex_compile              | 137 ms                                                     | 223 ms: 1.63x slower                                                |
| pprint_safe_repr           | 758 ms                                                     | 1.24 sec: 1.64x slower                                              |
| crypto_pyaes               | 77.5 ms                                                    | 127 ms: 1.65x slower                                                |
| chaos                      | 61.3 ms                                                    | 101 ms: 1.65x slower                                                |
| pprint_pformat             | 1.56 sec                                                   | 2.59 sec: 1.66x slower                                              |
| scimark_lu                 | 122 ms                                                     | 208 ms: 1.71x slower                                                |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 9.27 ms: 1.76x slower                                               |
| float                      | 78.9 ms                                                    | 139 ms: 1.76x slower                                                |
| pyflate                    | 484 ms                                                     | 880 ms: 1.82x slower                                                |
| nqueens                    | 81.4 ms                                                    | 151 ms: 1.86x slower                                                |
| mako                       | 11.2 ms                                                    | 20.9 ms: 1.86x slower                                               |
| unpickle_pure_python       | 218 us                                                     | 406 us: 1.86x slower                                                |
| fannkuch                   | 402 ms                                                     | 754 ms: 1.88x slower                                                |
| scimark_monte_carlo        | 69.2 ms                                                    | 138 ms: 1.99x slower                                                |
| spectral_norm              | 116 ms                                                     | 237 ms: 2.04x slower                                                |
| comprehensions             | 16.6 us                                                    | 35.2 us: 2.12x slower                                               |
| nbody                      | 88.3 ms                                                    | 203 ms: 2.30x slower                                                |
| hexiom                     | 6.30 ms                                                    | 15.1 ms: 2.40x slower                                               |
| Geometric mean             | (ref)                                                      | 1.23x slower                                                        |

Benchmark hidden because not significant (5): asyncio_websockets, json_dumps, xml_etree_parse, bench_mp_pool, djangocms
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 0.99x