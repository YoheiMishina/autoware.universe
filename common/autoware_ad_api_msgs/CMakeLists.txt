cmake_minimum_required(VERSION 3.14)
project(autoware_ad_api_msgs)

find_package(autoware_cmake REQUIRED)
autoware_package()

rosidl_generate_interfaces(${PROJECT_NAME}
  common/msg/ResponseStatus.msg
  interface/srv/InterfaceVersion.srv
  localization/msg/LocalizationInitializationState.msg
  localization/srv/InitializeLocalization.srv
  routing/msg/RouteState.msg
  routing/msg/Route.msg
  routing/msg/RouteData.msg
  routing/msg/RoutePrimitive.msg
  routing/msg/RouteSegment.msg
  routing/srv/ClearRoute.srv
  routing/srv/SetRoute.srv
  routing/srv/SetRoutePoints.srv
  DEPENDENCIES
    builtin_interfaces
    std_msgs
    geometry_msgs
)

ament_auto_package()
