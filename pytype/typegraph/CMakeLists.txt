add_package()

py_test(
  NAME
    cfg_test
  SRCS
    cfg_test.py
  DEPS
    .cfg
)

py_test(
  NAME
    cfg_utils_test
  SRCS
    cfg_utils_test.py
  DEPS
    .cfg
    pytype.cfg_utils
)

py_extension(
  NAME
    cfg
  SRCS
    cfg.cc
    cfg_logging.cc
    cfg_logging.h
    map_util.h
    memory_util.h
    pylogging.cc
    pylogging.h
    reachable.cc
    reachable.h
    solver.cc
    solver.h
    typegraph.cc
    typegraph.h
)
