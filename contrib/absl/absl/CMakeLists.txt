ADD_LIBRARY (absl_int128 STATIC
    numeric/int128.cc
)

TARGET_INCLUDE_DIRECTORIES (absl_int128
    PUBLIC ${PROJECT_SOURCE_DIR}/contrib/absl
)

ADD_LIBRARY (absl::int128 ALIAS absl_int128)

INSTALL(FILES base/attributes.h DESTINATION include/absl/base/)
INSTALL(FILES base/config.h DESTINATION include/absl/base/)
INSTALL(FILES base/macros.h DESTINATION include/absl/base/)
INSTALL(FILES base/optimization.h DESTINATION include/absl/base/)
INSTALL(FILES base/options.h DESTINATION include/absl/base/)
INSTALL(FILES base/policy_checks.h DESTINATION include/absl/base/)
INSTALL(FILES base/port.h DESTINATION include/absl/base/)
INSTALL(FILES base/internal/bits.h DESTINATION include/absl/base/internal/)
INSTALL(FILES numeric/int128.h DESTINATION include/absl/numeric/)
INSTALL(FILES numeric/int128_no_intrinsic.inc DESTINATION include/absl/numeric/)
INSTALL(FILES numeric/int128_have_intrinsic.inc DESTINATION include/absl/numeric/)